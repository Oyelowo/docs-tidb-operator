---
title: TiDB Operator 1.1 RC.4 Release Notes
---

# TiDB Operator 1.1 RC.4 Release Notes

Release date: May 15, 2020

TiDB Operator version: 1.1.0-rc.4

## Action Required

- Separate TiDB client certificates can be used for each component. Users should migrate the old TLS configs of Backup and Restore to the new configs. Refer to [#2403](https://github.com/pingcap/tidb-operator/pull/2403) for more details ([#2403](https://github.com/pingcap/tidb-operator/pull/2403), [@weekface](https://github.com/weekface))

## Other Notable Changes

- Fix the bug that the service annotations would be exposed in `TidbCluster` specification ([#2471](https://github.com/pingcap/tidb-operator/pull/2471), [@Yisaer](https://github.com/Yisaer))
- Fix a bug when reconciling TiDB service while the `healthCheckNodePort` is already generated by Kubernetes ([#2438](https://github.com/pingcap/tidb-operator/pull/2438), [@aylei](https://github.com/aylei))
- Support `TidbMonitorRef` in `TidbCluster` Status ([#2424](https://github.com/pingcap/tidb-operator/pull/2424), [@Yisaer](https://github.com/Yisaer))
- Support setting the backup path prefix for remote storage ([#2435](https://github.com/pingcap/tidb-operator/pull/2435), [@onlymellb](https://github.com/onlymellb))
- Support customizing `mydumper` options in Backup CR ([#2407](https://github.com/pingcap/tidb-operator/pull/2407), [@onlymellb](https://github.com/onlymellb))
- Support TiCDC in TidbCluster CR. ([#2338](https://github.com/pingcap/tidb-operator/pull/2338), [@weekface](https://github.com/weekface))
- Update BR to `v3.1.1` in the `tidb-backup-manager` image ([#2425](https://github.com/pingcap/tidb-operator/pull/2425), [@DanielZhangQD](https://github.com/DanielZhangQD))
- Support creating node pools for TiFlash and CDC on ACK ([#2420](https://github.com/pingcap/tidb-operator/pull/2420), [@DanielZhangQD](https://github.com/DanielZhangQD))
- Support creating node pools for TiFlash and CDC on EKS ([#2413](https://github.com/pingcap/tidb-operator/pull/2413), [@DanielZhangQD](https://github.com/DanielZhangQD))
- Expose `PVReclaimPolicy` for `TidbMonitor` when storage is enabled ([#2379](https://github.com/pingcap/tidb-operator/pull/2379), [@Yisaer](https://github.com/Yisaer))
- Support arbitrary topology-based HA in tidb-scheduler (e.g. node zones) ([#2366](https://github.com/pingcap/tidb-operator/pull/2366), [@PengJi](https://github.com/PengJi))
- Skip setting the TLS for PD dashboard when the TiDB version is earlier than 4.0.0 ([#2389](https://github.com/pingcap/tidb-operator/pull/2389), [@weekface](https://github.com/weekface))
- Support backup and restore with GCS using BR ([#2267](https://github.com/pingcap/tidb-operator/pull/2267), [@shuijing198799](https://github.com/shuijing198799))
- Update `TiDBConfig` and `TiKVConfig` to support the `4.0.0-rc` version ([#2322](https://github.com/pingcap/tidb-operator/pull/2322), [@Yisaer](https://github.com/Yisaer))
- Fix the bug when `TidbCluster` service type is `NodePort`, the value of `NodePort` would change frequently ([#2284](https://github.com/pingcap/tidb-operator/pull/2284), [@Yisaer](https://github.com/Yisaer))
- Add external strategy ability for `TidbClusterAutoScaler` ([#2279](https://github.com/pingcap/tidb-operator/pull/2279), [@Yisaer](https://github.com/Yisaer))
- PVC will not be deleted when `TidbMonitor` gets deleted ([#2374](https://github.com/pingcap/tidb-operator/pull/2374), [@Yisaer](https://github.com/Yisaer))
- Support scaling for TiFlash ([#2237](https://github.com/pingcap/tidb-operator/pull/2237), [@DanielZhangQD](https://github.com/DanielZhangQD))