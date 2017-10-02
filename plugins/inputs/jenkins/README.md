# Telegraf Plugin: Jenkins

This plugin will read information from [Jenkins Metrics Plugin](https://wiki.jenkins.io/display/JENKINS/Metrics+Plugin)
(should be installed on jenkins server).

### Configuration:

Install [Jenkins Metrics Plugin](https://wiki.jenkins.io/display/JENKINS/Metrics+Plugin) on your jenkins, and generate
access token by global configuration screen (<jenkins-url>/configure) under the “Metrics” section.

```toml
# Jenkins server 1
[[inputs.jenkins.servers]]
    url = "http://127.0.0.1:8080"
    token = "wvS2XYTNQf6K3Wciht17cBGJs9SKB_DFSYTDDG5mc-JYBPEhA6Tpc5LVcTlogUP1"

# Jenkins server 2
[[inputs.jenkins.servers]]
    url = "http://10.0.0.1"
    token = "aasda1qdakdsaldkamdlk012e"
```

### Tags:

- All measurements have the following tags:
    - type   - type of metrics (counters, gauges, timers, metrics)
    - server - address of your server

### Fields

```
http.activeRequests.count
http.requests.count
http.requests.m15_rate
http.requests.m1_rate
http.requests.m5_rate
http.requests.max
http.requests.mean
http.requests.mean_rate
http.requests.min
http.requests.p50
http.requests.p75
http.requests.p95
http.requests.p98
http.requests.p99
http.requests.p999
http.requests.stddev
http.responseCodes.badRequest.count
http.responseCodes.badRequest.m15_rate
http.responseCodes.badRequest.m1_rate
http.responseCodes.badRequest.m5_rate
http.responseCodes.badRequest.mean_rate
http.responseCodes.created.count
http.responseCodes.created.m15_rate
http.responseCodes.created.m1_rate
http.responseCodes.created.m5_rate
http.responseCodes.created.mean_rate
http.responseCodes.forbidden.count
http.responseCodes.forbidden.m15_rate
http.responseCodes.forbidden.m1_rate
http.responseCodes.forbidden.m5_rate
http.responseCodes.forbidden.mean_rate
http.responseCodes.noContent.count
http.responseCodes.noContent.m15_rate
http.responseCodes.noContent.m1_rate
http.responseCodes.noContent.m5_rate
http.responseCodes.noContent.mean_rate
http.responseCodes.notFound.count
http.responseCodes.notFound.m15_rate
http.responseCodes.notFound.m1_rate
http.responseCodes.notFound.m5_rate
http.responseCodes.notFound.mean_rate
http.responseCodes.notModified.count
http.responseCodes.notModified.m15_rate
http.responseCodes.notModified.m1_rate
http.responseCodes.notModified.m5_rate
http.responseCodes.notModified.mean_rate
http.responseCodes.ok.count
http.responseCodes.ok.m15_rate
http.responseCodes.ok.m1_rate
http.responseCodes.ok.m5_rate
http.responseCodes.ok.mean_rate
http.responseCodes.other.count
http.responseCodes.other.m15_rate
http.responseCodes.other.m1_rate
http.responseCodes.other.m5_rate
http.responseCodes.other.mean_rate
http.responseCodes.serverError.count
http.responseCodes.serverError.m15_rate
http.responseCodes.serverError.m1_rate
http.responseCodes.serverError.m5_rate
http.responseCodes.serverError.mean_rate
http.responseCodes.serviceUnavailable.count
http.responseCodes.serviceUnavailable.m15_rate
http.responseCodes.serviceUnavailable.m1_rate
http.responseCodes.serviceUnavailable.m5_rate
http.responseCodes.serviceUnavailable.mean_rate
jenkins.executor.count.value.value
jenkins.executor.free.value.value
jenkins.executor.in-use.value.value
jenkins.health-check.count.value
jenkins.health-check.duration.count
jenkins.health-check.duration.m15_rate
jenkins.health-check.duration.m1_rate
jenkins.health-check.duration.m5_rate
jenkins.health-check.duration.max
jenkins.health-check.duration.mean
jenkins.health-check.duration.mean_rate
jenkins.health-check.duration.min
jenkins.health-check.duration.p50
jenkins.health-check.duration.p75
jenkins.health-check.duration.p95
jenkins.health-check.duration.p98
jenkins.health-check.duration.p99
jenkins.health-check.duration.p999
jenkins.health-check.duration.stddev
jenkins.health-check.inverse-score.value
jenkins.health-check.score.value
jenkins.job.averageDepth.value
jenkins.job.blocked.duration.count
jenkins.job.blocked.duration.m15_rate
jenkins.job.blocked.duration.m1_rate
jenkins.job.blocked.duration.m5_rate
jenkins.job.blocked.duration.max
jenkins.job.blocked.duration.mean
jenkins.job.blocked.duration.mean_rate
jenkins.job.blocked.duration.min
jenkins.job.blocked.duration.p50
jenkins.job.blocked.duration.p75
jenkins.job.blocked.duration.p95
jenkins.job.blocked.duration.p98
jenkins.job.blocked.duration.p99
jenkins.job.blocked.duration.p999
jenkins.job.blocked.duration.stddev
jenkins.job.buildable.duration.count
jenkins.job.buildable.duration.m15_rate
jenkins.job.buildable.duration.m1_rate
jenkins.job.buildable.duration.m5_rate
jenkins.job.buildable.duration.max
jenkins.job.buildable.duration.mean
jenkins.job.buildable.duration.mean_rate
jenkins.job.buildable.duration.min
jenkins.job.buildable.duration.p50
jenkins.job.buildable.duration.p75
jenkins.job.buildable.duration.p95
jenkins.job.buildable.duration.p98
jenkins.job.buildable.duration.p99
jenkins.job.buildable.duration.p999
jenkins.job.buildable.duration.stddev
jenkins.job.building.duration.count
jenkins.job.building.duration.m15_rate
jenkins.job.building.duration.m1_rate
jenkins.job.building.duration.m5_rate
jenkins.job.building.duration.max
jenkins.job.building.duration.mean
jenkins.job.building.duration.mean_rate
jenkins.job.building.duration.min
jenkins.job.building.duration.p50
jenkins.job.building.duration.p75
jenkins.job.building.duration.p95
jenkins.job.building.duration.p98
jenkins.job.building.duration.p99
jenkins.job.building.duration.p999
jenkins.job.building.duration.stddev
jenkins.job.count.value.value
jenkins.job.queuing.duration.count
jenkins.job.queuing.duration.m15_rate
jenkins.job.queuing.duration.m1_rate
jenkins.job.queuing.duration.m5_rate
jenkins.job.queuing.duration.max
jenkins.job.queuing.duration.mean
jenkins.job.queuing.duration.mean_rate
jenkins.job.queuing.duration.min
jenkins.job.queuing.duration.p50
jenkins.job.queuing.duration.p75
jenkins.job.queuing.duration.p95
jenkins.job.queuing.duration.p98
jenkins.job.queuing.duration.p99
jenkins.job.queuing.duration.p999
jenkins.job.queuing.duration.stddev
jenkins.job.scheduled.count
jenkins.job.scheduled.m15_rate
jenkins.job.scheduled.m1_rate
jenkins.job.scheduled.m5_rate
jenkins.job.scheduled.mean_rate
jenkins.job.total.duration.count
jenkins.job.total.duration.m15_rate
jenkins.job.total.duration.m1_rate
jenkins.job.total.duration.m5_rate
jenkins.job.total.duration.max
jenkins.job.total.duration.mean
jenkins.job.total.duration.mean_rate
jenkins.job.total.duration.min
jenkins.job.total.duration.p50
jenkins.job.total.duration.p75
jenkins.job.total.duration.p95
jenkins.job.total.duration.p98
jenkins.job.total.duration.p99
jenkins.job.total.duration.p999
jenkins.job.total.duration.stddev
jenkins.job.waiting.duration.count
jenkins.job.waiting.duration.m15_rate
jenkins.job.waiting.duration.m1_rate
jenkins.job.waiting.duration.m5_rate
jenkins.job.waiting.duration.max
jenkins.job.waiting.duration.mean
jenkins.job.waiting.duration.mean_rate
jenkins.job.waiting.duration.min
jenkins.job.waiting.duration.p50
jenkins.job.waiting.duration.p75
jenkins.job.waiting.duration.p95
jenkins.job.waiting.duration.p98
jenkins.job.waiting.duration.p99
jenkins.job.waiting.duration.p999
jenkins.job.waiting.duration.stddev
jenkins.node.count.value.value
jenkins.node.offline.value.value
jenkins.node.online.value.value
jenkins.plugins.active.value
jenkins.plugins.failed.value
jenkins.plugins.inactive.value
jenkins.plugins.withUpdate.value
jenkins.project.count.value.value
jenkins.project.disabled.count.value.value
jenkins.project.enabled.count.value.value
jenkins.queue.blocked.value.value
jenkins.queue.buildable.value.value
jenkins.queue.pending.value.value
jenkins.queue.size.value.value
jenkins.queue.stuck.value.value
jenkins.runs.aborted.count
jenkins.runs.aborted.m15_rate
jenkins.runs.aborted.m1_rate
jenkins.runs.aborted.m5_rate
jenkins.runs.aborted.mean_rate
jenkins.runs.failure.count
jenkins.runs.failure.m15_rate
jenkins.runs.failure.m1_rate
jenkins.runs.failure.m5_rate
jenkins.runs.failure.mean_rate
jenkins.runs.not_built.count
jenkins.runs.not_built.m15_rate
jenkins.runs.not_built.m1_rate
jenkins.runs.not_built.m5_rate
jenkins.runs.not_built.mean_rate
jenkins.runs.success.count
jenkins.runs.success.m15_rate
jenkins.runs.success.m1_rate
jenkins.runs.success.m5_rate
jenkins.runs.success.mean_rate
jenkins.runs.total.count
jenkins.runs.total.m15_rate
jenkins.runs.total.m1_rate
jenkins.runs.total.m5_rate
jenkins.runs.total.mean_rate
jenkins.runs.unstable.count
jenkins.runs.unstable.m15_rate
jenkins.runs.unstable.m1_rate
jenkins.runs.unstable.m5_rate
jenkins.runs.unstable.mean_rate
system.cpu.load.value
vm.blocked.count.value
vm.class.loaded.value
vm.class.unloaded.value
vm.count.value
vm.cpu.load.value
vm.daemon.count.value
vm.deadlock.count.value
vm.file.descriptor.ratio.value
vm.gc.PS-MarkSweep.count.value
vm.gc.PS-MarkSweep.time.value
vm.gc.PS-Scavenge.count.value
vm.gc.PS-Scavenge.time.value
vm.memory.heap.committed.value
vm.memory.heap.init.value
vm.memory.heap.max.value
vm.memory.heap.usage.value
vm.memory.heap.used.value
vm.memory.non-heap.committed.value
vm.memory.non-heap.init.value
vm.memory.non-heap.max.value
vm.memory.non-heap.usage.value
vm.memory.non-heap.used.value
vm.memory.pools.Code-Cache.committed.value
vm.memory.pools.Code-Cache.init.value
vm.memory.pools.Code-Cache.max.value
vm.memory.pools.Code-Cache.usage.value
vm.memory.pools.Code-Cache.used.value
vm.memory.pools.Compressed-Class-Space.committed.value
vm.memory.pools.Compressed-Class-Space.init.value
vm.memory.pools.Compressed-Class-Space.max.value
vm.memory.pools.Compressed-Class-Space.usage.value
vm.memory.pools.Compressed-Class-Space.used.value
vm.memory.pools.Metaspace.committed.value
vm.memory.pools.Metaspace.init.value
vm.memory.pools.Metaspace.max.value
vm.memory.pools.Metaspace.usage.value
vm.memory.pools.Metaspace.used.value
vm.memory.pools.PS-Eden-Space.committed.value
vm.memory.pools.PS-Eden-Space.init.value
vm.memory.pools.PS-Eden-Space.max.value
vm.memory.pools.PS-Eden-Space.usage.value
vm.memory.pools.PS-Eden-Space.used.value
vm.memory.pools.PS-Old-Gen.committed.value
vm.memory.pools.PS-Old-Gen.init.value
vm.memory.pools.PS-Old-Gen.max.value
vm.memory.pools.PS-Old-Gen.usage.value
vm.memory.pools.PS-Old-Gen.used.value
vm.memory.pools.PS-Survivor-Space.committed.value
vm.memory.pools.PS-Survivor-Space.init.value
vm.memory.pools.PS-Survivor-Space.max.value
vm.memory.pools.PS-Survivor-Space.usage.value
vm.memory.pools.PS-Survivor-Space.used.value
vm.memory.total.committed.value
vm.memory.total.init.value
vm.memory.total.max.value
vm.memory.total.used.value
vm.new.count.value
vm.runnable.count.value
vm.terminated.count.value
vm.timed_waiting.count.value
vm.uptime.milliseconds.value
vm.waiting.count.value
```