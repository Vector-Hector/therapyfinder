![therapynowlogo.png](therapynowlogo.png)

Therapy now is a concept project for the [2025 {Tech: Europe} Berlin AI Hackathon](https://lu.ma/berlin-hackathon).
It is an AI voice agent that talks to patients looking for therapy spots in
Germany. It will try to find out what the best parameters for the search
would be. This includes:

- The patient's info
  - Email
  - Name
  - Location
  - Insurance type
- The suggested/preferred therapy types

With these parameters, the agent will search through a database of therapists.
A special focus is public health insurance for this project. It is currently
**not** connected to any live API. But it would be possible to hook into [kvberlin](https://github.com/Vector-Hector/kvberlin)
for instance if provided the necessary permissions. 

Now, it will contact therapists via email and wait for their responses. With a
timeout of 7 days. This process is simplified for demonstration purposes to a dummy 
api call simulated through choosing a random document in [example_responses](./example_responses).
Timeout is 30% probability as well.

A GPT model then interprets and categorizes the therapist's responses. Finally,
it will output a report pdf to the user. In case there is no therapist with a
therapy spot available, 