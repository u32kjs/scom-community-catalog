OpsMgr Health State Synchronization MP
======================================

![HealthSync80](http://www.tyconsulting.com.au/wp-content/uploads/2015/04/HealthSync80.png)It is common to have multiple OpsMgr management groups in large organizations. When designing distributed application or creating custom dashboards, one of the limitations is that OpsMgr users can only select monitoring objects within the local management group to be a part of the Health Model. This becomes an issue when users want to design a Distributed Application or dashboard that include components monitored by different OpsMgr management groups.

The?OpsMgr Health Synchronization Library?management pack is designed to provide a workaround to this limitation. This management pack provides a template that enables OpsMgr users to create monitoring objects named "Health State Watcher" hosted by All Management Servers Resource Pool. Health State Watcher objects have monitors configured to query health state of monitoring objects located in a remote management group using OpsMgr SDK.

[![HealthStateSyncMPDiagram](http://www.tyconsulting.com.au/wp-content/uploads/2015/04/HealthStateSyncMPDiagram-700x311.png)](http://www.tyconsulting.com.au/wp-content/uploads/2015/04/HealthStateSyncMPDiagram.png)

As shown in the diagram above, an instance of Health State Watcher can be created for each monitoring object of user's choice from a remote management group. Each Health State Watcher object will periodically update its own health state based on the health state of the remote monitoring object it is watching for (every 5 minutes by default). As shown above, the Health State Watcher can query health state of any monitoring objects from remote management group (i.e. a Windows Computer object, a Distributed Application or any other types monitoring objects).
