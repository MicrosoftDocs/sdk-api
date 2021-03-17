---
UID: NF:clusapi.RegisterClusterNotify
title: RegisterClusterNotify function (clusapi.h)
description: Adds an event type to the list of events stored for a notification port.
helpviewer_keywords: ["CLUSTER_CHANGE_CLUSTER_PROPERTY","CLUSTER_CHANGE_CLUSTER_RECONNECT","CLUSTER_CHANGE_CLUSTER_STATE","CLUSTER_CHANGE_GROUP_ADDED","CLUSTER_CHANGE_GROUP_DELETED","CLUSTER_CHANGE_GROUP_PROPERTY","CLUSTER_CHANGE_GROUP_STATE","CLUSTER_CHANGE_HANDLE_CLOSE","CLUSTER_CHANGE_NETINTERFACE_ADDED","CLUSTER_CHANGE_NETINTERFACE_DELETED","CLUSTER_CHANGE_NETINTERFACE_PROPERTY","CLUSTER_CHANGE_NETINTERFACE_STATE","CLUSTER_CHANGE_NETWORK_ADDED","CLUSTER_CHANGE_NETWORK_DELETED","CLUSTER_CHANGE_NETWORK_PROPERTY","CLUSTER_CHANGE_NETWORK_STATE","CLUSTER_CHANGE_NODE_ADDED","CLUSTER_CHANGE_NODE_DELETED","CLUSTER_CHANGE_NODE_PROPERTY","CLUSTER_CHANGE_NODE_STATE","CLUSTER_CHANGE_QUORUM_STATE","CLUSTER_CHANGE_REGISTRY_ATTRIBUTES","CLUSTER_CHANGE_REGISTRY_NAME","CLUSTER_CHANGE_REGISTRY_SUBTREE","CLUSTER_CHANGE_REGISTRY_VALUE","CLUSTER_CHANGE_RESOURCE_ADDED","CLUSTER_CHANGE_RESOURCE_DELETED","CLUSTER_CHANGE_RESOURCE_PROPERTY","CLUSTER_CHANGE_RESOURCE_STATE","CLUSTER_CHANGE_RESOURCE_TYPE_ADDED","CLUSTER_CHANGE_RESOURCE_TYPE_DELETED","CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY","PCLUSAPI_REGISTER_CLUSTER_NOTIFY","PCLUSAPI_REGISTER_CLUSTER_NOTIFY function [Failover Cluster]","RegisterClusterNotify","RegisterClusterNotify function [Failover Cluster]","_wolf_registerclusternotify","clusapi/PCLUSAPI_REGISTER_CLUSTER_NOTIFY","clusapi/RegisterClusterNotify","mscs.registerclusternotify"]
old-location: mscs\registerclusternotify.htm
tech.root: MsCS
ms.assetid: ddf0e01c-08e9-4e32-b012-76c8a41037a7
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_CLUSTER_PROPERTY, CLUSTER_CHANGE_CLUSTER_RECONNECT, CLUSTER_CHANGE_CLUSTER_STATE, CLUSTER_CHANGE_GROUP_ADDED, CLUSTER_CHANGE_GROUP_DELETED, CLUSTER_CHANGE_GROUP_PROPERTY, CLUSTER_CHANGE_GROUP_STATE, CLUSTER_CHANGE_HANDLE_CLOSE, CLUSTER_CHANGE_NETINTERFACE_ADDED, CLUSTER_CHANGE_NETINTERFACE_DELETED, CLUSTER_CHANGE_NETINTERFACE_PROPERTY, CLUSTER_CHANGE_NETINTERFACE_STATE, CLUSTER_CHANGE_NETWORK_ADDED, CLUSTER_CHANGE_NETWORK_DELETED, CLUSTER_CHANGE_NETWORK_PROPERTY, CLUSTER_CHANGE_NETWORK_STATE, CLUSTER_CHANGE_NODE_ADDED, CLUSTER_CHANGE_NODE_DELETED, CLUSTER_CHANGE_NODE_PROPERTY, CLUSTER_CHANGE_NODE_STATE, CLUSTER_CHANGE_QUORUM_STATE, CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, CLUSTER_CHANGE_REGISTRY_NAME, CLUSTER_CHANGE_REGISTRY_SUBTREE, CLUSTER_CHANGE_REGISTRY_VALUE, CLUSTER_CHANGE_RESOURCE_ADDED, CLUSTER_CHANGE_RESOURCE_DELETED, CLUSTER_CHANGE_RESOURCE_PROPERTY, CLUSTER_CHANGE_RESOURCE_STATE, CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, PCLUSAPI_REGISTER_CLUSTER_NOTIFY, PCLUSAPI_REGISTER_CLUSTER_NOTIFY function [Failover Cluster], RegisterClusterNotify, RegisterClusterNotify function [Failover Cluster], _wolf_registerclusternotify, clusapi/PCLUSAPI_REGISTER_CLUSTER_NOTIFY, clusapi/RegisterClusterNotify, mscs.registerclusternotify
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterClusterNotify
 - clusapi/RegisterClusterNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - RegisterClusterNotify
---

# RegisterClusterNotify function


## -description

Adds an 
    event type to the list of events stored for a notification port. The <b>PCLUSAPI_REGISTER_CLUSTER_NOTIFY</b> type defines a pointer to this function.

## -parameters

### -param hChange [in]

Handle to a notification port created with the 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a> function.

### -param dwFilterType [in]

Bitmask of flags that describes the event to be added to the set of events currently being monitored by the 
      notification port. For more information about these event types, see 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a>. The 
      <i>dwFilterType</i> parameter can be set to one of the following flags.



#### CLUSTER_CHANGE_CLUSTER_PROPERTY (0x40000000)

The queue receives a notification when the cluster's prioritized list of internal 
        <a href="/previous-versions/windows/desktop/mscs/networks">networks</a> changes.



#### CLUSTER_CHANGE_CLUSTER_RECONNECT

The queue receives a notification when the connection to the cluster identified by 
        <i>hCluster</i> is reestablished after a brief disconnect. Some events generated 
        immediately before or after this event may have been lost. You need to close all open connections and 
        reconnect to receive accurate state information.



#### CLUSTER_CHANGE_CLUSTER_STATE (0x20000000)

The queue receives a notification when the cluster becomes unavailable, meaning that all attempts to communicate with the cluster fail. This notification is reserved for future use.



#### CLUSTER_CHANGE_GROUP_ADDED (0x00004000)

The queue receives a notification when a new <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is 
        created in the cluster.



#### CLUSTER_CHANGE_GROUP_DELETED (0x00002000)

The queue receives a notification when an existing 
        <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is deleted.



#### CLUSTER_CHANGE_GROUP_PROPERTY (0x00008000)

The queue receives a notification when the 
        <a href="/previous-versions/windows/desktop/mscs/group-common-properties">properties</a> of an existing group change.



#### CLUSTER_CHANGE_GROUP_STATE (0x00001000)

The queue receives a notification when a group changes state.



#### CLUSTER_CHANGE_HANDLE_CLOSE (0x80000000)

The queue receives a notification when a handle to a 
        <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a> is closed.



#### CLUSTER_CHANGE_NETINTERFACE_ADDED (0x04000000)

The queue receives a notification when a new 
        <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a> is added to a cluster 
        <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.



#### CLUSTER_CHANGE_NETINTERFACE_DELETED (0x02000000)

The queue receives a notification when a network interface is permanently removed from a cluster node.



#### CLUSTER_CHANGE_NETINTERFACE_PROPERTY (0x08000000)

The queue receives a notification when the 
        <a href="/previous-versions/windows/desktop/mscs/network-interface-common-properties">properties</a> of an existing network interface change.



#### CLUSTER_CHANGE_NETINTERFACE_STATE (0x01000000)

The queue receives a notification when a network interface changes state. For a list of the possible 
        network interface state values, see 
        <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetinterfacestate">GetClusterNetInterfaceState</a>.



#### CLUSTER_CHANGE_NETWORK_ADDED (0x00400000)

The queue receives a notification when a new 
        <a href="/previous-versions/windows/desktop/mscs/networks">network</a> is added to the cluster environment.



#### CLUSTER_CHANGE_NETWORK_DELETED (0x00200000)

The queue receives a notification when a network is permanently removed from the cluster environment.



#### CLUSTER_CHANGE_NETWORK_PROPERTY (0x00800000)

The queue receives a notification when the  <a href="/previous-versions/windows/desktop/mscs/network-common-properties">properties</a> of an existing network change.



#### CLUSTER_CHANGE_NETWORK_STATE (0x00100000)

The queue receives a notification when a network changes state. For a list of the possible network state values, see  <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetworkstate">GetClusterNetworkState</a>.



#### CLUSTER_CHANGE_NODE_ADDED (0x00000004)

The queue receives a notification when a new  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> is added to the cluster. A node can be added only when the Cluster service is initially installed on the node.



#### CLUSTER_CHANGE_NODE_DELETED (0x00000002)

The queue receives a notification when a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> is permanently removed from a cluster. A node can be permanently deleted from an existing cluster with a call to the  <a href="/windows/desktop/api/clusapi/nf-clusapi-evictclusternode">EvictClusterNode</a> function.



#### CLUSTER_CHANGE_NODE_PROPERTY (0x00000008)

This notification is reserved for future use.



#### CLUSTER_CHANGE_NODE_STATE (0x00000001)

The queue receives a notification when a node changes state.



#### CLUSTER_CHANGE_QUORUM_STATE (0x10000000)

The queue receives a notification when the  <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a> changes state.



#### CLUSTER_CHANGE_REGISTRY_ATTRIBUTES (0x00000020)

The queue receives a notification when a  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key's attributes are changed.



#### CLUSTER_CHANGE_REGISTRY_NAME (0x00000010)

The queue receives a notification when a change to a name is made in the cluster database.



#### CLUSTER_CHANGE_REGISTRY_SUBTREE (0x00000080)

Indicates that the other CLUSTER_CHANGE_REGISTRY events apply to the root of the cluster database and to all of the subkeys. If CLUSTER_CHANGE_REGISTRY_SUBTREE is not specified, the notifications apply only to the root.



#### CLUSTER_CHANGE_REGISTRY_VALUE (0x00000040)

The queue receives a notification when a value of the specified cluster database key is changed or deleted.



#### CLUSTER_CHANGE_RESOURCE_ADDED (0x00000400)

The queue receives a notification when a new  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is created in the cluster.



#### CLUSTER_CHANGE_RESOURCE_DELETED (0x00000200)

The queue receives a notification when a 
        <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is deleted.



#### CLUSTER_CHANGE_RESOURCE_PROPERTY (0x00000800)

Indicates that a notification should be issued when the 
        <a href="/previous-versions/windows/desktop/mscs/resource-common-properties">properties</a> of a resource change.



#### CLUSTER_CHANGE_RESOURCE_STATE (0x00000100)

The queue receives a notification when a resource changes state.



#### CLUSTER_CHANGE_RESOURCE_TYPE_ADDED (0x00020000)

The queue receives a notification when a new 
        <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> is created in the cluster.



#### CLUSTER_CHANGE_RESOURCE_TYPE_DELETED (0x00010000)

The queue receives a notification when an existing resource type is deleted.



#### CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY (0x00040000)

The queue receives a notification when the 
        <a href="/previous-versions/windows/desktop/mscs/resource-common-properties">properties</a> of a resource type change.

### -param hObject [in]

Handle to the <a href="/previous-versions/windows/desktop/mscs/cluster-objects">failover cluster object</a> 
      affected by the event specified in the <i>dwFilterType</i> parameter. The type of handle 
      depends on the value of <i>dwFilterType</i> as described in the following list.



#### CLUSTER_CHANGE_CLUSTER_PROPERTY

<b>HCLUSTER</b>



#### CLUSTER_CHANGE_CLUSTER_STATE

<b>HCLUSTER</b>



#### CLUSTER_CHANGE_GROUP_DELETED

<b>HGROUP</b>



#### CLUSTER_CHANGE_GROUP_PROPERTY

<b>HGROUP</b>



#### CLUSTER_CHANGE_GROUP_STATE

<b>HGROUP</b>



#### CLUSTER_CHANGE_HANDLE_CLOSE

<b>HCLUSTER</b>, if the flag is used by itself; otherwise, the handle that is associated with the flag that <b>CLUSTER_CHANGE_HANDLE_CLOSE</b> is combined with becomes the handle type.

For example, if the value of the  <i>dwFilterType</i> parameter is <b>CLUSTER_CHANGE_GROUP_PROPERTY</b> | <b>CLUSTER_CHANGE_HANDLE_CLOSE</b>, then the type of handle for the  <i>hObject</i> parameter becomes <b>HGROUP</b>, because the <b>CLUSTER_CHANGE_GROUP_PROPERTY</b> flag is associated with the <b>HGROUP</b> handle type.



#### CLUSTER_CHANGE_NODE_DELETED

<b>HNODE</b>



#### CLUSTER_CHANGE_NODE_PROPERTY

<b>HNODE</b>



#### CLUSTER_CHANGE_NODE_STATE

<b>HNODE</b>



#### CLUSTER_CHANGE_REGISTRY_ATTRIBUTES

<b>HKEY</b>



#### CLUSTER_CHANGE_REGISTRY_NAME

<b>HKEY</b>



#### CLUSTER_CHANGE_REGISTRY_SUBTREE

<b>HKEY</b>



#### CLUSTER_CHANGE_REGISTRY_VALUE

<b>HKEY</b>



#### CLUSTER_CHANGE_RESOURCE_DELETED

<b>HRESOURCE</b>



#### CLUSTER_CHANGE_RESOURCE_PROPERTY

<b>HRESOURCE</b>



#### CLUSTER_CHANGE_RESOURCE_STATE

<b>HRESOURCE</b>

The cluster database functions return a valid cluster database key that can be used to set 
       <i>hObject</i> when <i>dwFilterType</i> is set to an event type affecting 
       the cluster database.

### -param dwNotifyKey [in]

Notification key returned from 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a> when the requested event 
      occurs.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The  <b>RegisterClusterNotify</b> function enables an application that has already created a notification port with  <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a> to register for an additional event that affects a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>,  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>, or  <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.

To receive notifications of 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> changes, one or more of the 
    flags applicable to the database must be set in the <i>dwFilterType</i> parameter. Applicable 
    flags start with the prefix CLUSTER_CHANGE_REGISTRY. Making manual changes to the cluster database through the 
    registry editor, RegEdit.exe, does not generate notifications.


#### Examples

See the <a href="/previous-versions/windows/desktop/mscs/notification-port-example">Notification Port Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternotifyport">CloseClusterNotifyPort</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a>