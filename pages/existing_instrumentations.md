---
title: Existing instrumentations
weight: 3
---

Tracing information is collected on each host using the instrumented libraries
and sent to Zipkin. When the host makes a request to another service, it passes
a few tracing identifers along with the request so we can later tie the data
together.

The following libraries exist to provide instrumentation on various platforms.
Please refer to their individual documentation for setup and configuration
guides.

| Language | Library | Framework | Transports Supported | Sampling Supported? | Other notes |
|:---------|:--------|:----------|:---------------------|:--------------------|:------------|{% for lib in site.data.existing_instrumentations %}
| {{ lib.language }} | {{ lib.library }} | {{ lib.framework }} | {{ lib.transports }} | {{ lib.sampling }} | {{ lib.notes }} |{% endfor %}
{: .wide-table}

Did we miss a library? Please open a pull-request to
[openzipkin.github.io](https://github.com/openzipkin/openzipkin.github.io).

Want to create instrumentation for another framework / platform? We have documentation on [instrumenting a library]({{ site.github.url }}/pages/instrumenting).
