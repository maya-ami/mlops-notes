### MLOps
We can achieve faster and cleaner ML operations using:
- Experiment tracker and Model registry for reproducibility (Module 2).
- ML pipelines which allow run multiple experiments without changes in the code in a clean way (Module 3).
- Monitoring services that would trigger an alarm in case of the metrics drop. If the system's mature enough, the monitoring might be done without the human in the loop: the drop in metrics will automatically re-launch the ML pipeline with the updated data/parameters and deploy a new model to production.


### MLOps maturity model
Levels:
- 0: No MLOps. 
	All code in JN, no automation. A typical situation of DS working in isolation. OK to be on this level for the proof of concept cases.
- 1: DevOps, but no MLOps.
	Releases are automated, there're unit & integration tests, CI/CD, Ops metrics. But the Ops are not specific to ML: no experiment tracking; no reproducibility; DS are separated from engineers. 
- 2: Automated training.
	There's a training pipeline, experiment tracking, and model registry. The team is aware of the model in production and its parameters. Low friction deployment. DS work with engineers.
- 3: Automated deployment.
	No need for human. Easy to deploy a model. There's an ML platform for hosting ML models. DS make API calls to the ML platform which provides a URL with the address where the model is available.
The ML platform has a capability of running A/B tests.
Models are monitored.
- 4: Full MLOps Automated Operations.
	Automated training, re-training, and deployment. Might be dangerous to exclude a human from the loop at all, as we want to make sure that ML models are reliable.
	