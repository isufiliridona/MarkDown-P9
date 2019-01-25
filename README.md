# MarkDown-P9
MarkDown 

Loki Logo
CircleCI Go Report Card Slack

Loki: like Prometheus, but for logs.
Loki is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus. It is designed to be very cost effective and easy to operate, as it does not index the contents of the logs, but rather a set of labels for each log stream.

Compared to other log aggregation systems, Loki:

does not do full text indexing on logs. By storing compressed, unstructured logs and only indexing metadata, Loki is simpler to operate and cheaper to run.
indexes and groups log streams using the same labels you’re already using with Prometheus, enabling you to seamlessly switch between metrics and logs using the same labels that you’re already using with Prometheus.
is an especially good fit for storing Kubernetes Pod logs. Metadata such as Pod labels is automatically scraped and indexed.
has native support in Grafana (already in the nightly builds, will be included in Grafana 6.0).
A Loki-based logging stack consists of 3 components:

promtail is the agent, responsible for gathering logs and sending them to Loki.
loki is the main server, responsible for storing logs and processing queries.
Grafana for the UI.
Loki is like Prometheus, but for logs: we prefer a multidimensional label-based approach to indexing, and want a single-binary, easy to operate system with no dependencies. Loki differs from Prometheus by focussing on logs instead of metrics, and delivering logs via push, instead of pull.

Getting started
For instructions on getting started with Loki, see our getting started docs.

For the beginnings of documentation on how to use Loki, see our usage docs. API documentation is also available.

Getting Help
If you have any questions or feedback regarding Loki:

Ask a question on the Loki Slack channel. To invite yourself to the Grafana Slack, visit http://slack.raintank.io/ and join the #loki channel.
File an issue for bugs, issues and feature suggestions.
Send an email to lokiproject@googlegroups.com, or use the web interface.
UI issues should be filed directly in Grafana.
Your feedback is always welcome.

Further Reading
The original design doc for Loki is a good source for discussion of the motivation and design decisions.
David Kaltschmidt's OSMC 2018 talk "Logging is coming to Grafana"
David Kaltschmidt's KubeCon 2018 talk "On the OSS Path to Full Observability with Grafana" (slides, video)
Goutham Veeramachaneni's blog post "Loki: Prometheus-inspired, open source logging for cloud natives".
