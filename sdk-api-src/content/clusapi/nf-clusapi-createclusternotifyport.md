---
UID: NF:clusapi.CreateClusterNotifyPort
title: CreateClusterNotifyPort function (clusapi.h)
description: Creates or modifies a notification port. For information on notification ports, see Receiving Cluster Events.
helpviewer_keywords: ["CLUSTER_CHANGE_CLUSTER_PROPERTY","CLUSTER_CHANGE_CLUSTER_RECONNECT","CLUSTER_CHANGE_CLUSTER_STATE","CLUSTER_CHANGE_GROUP_ADDED","CLUSTER_CHANGE_GROUP_DELETED","CLUSTER_CHANGE_GROUP_PROPERTY","CLUSTER_CHANGE_GROUP_STATE","CLUSTER_CHANGE_HANDLE_CLOSE","CLUSTER_CHANGE_NETINTERFACE_ADDED","CLUSTER_CHANGE_NETINTERFACE_DELETED","CLUSTER_CHANGE_NETINTERFACE_PROPERTY","CLUSTER_CHANGE_NETINTERFACE_STATE","CLUSTER_CHANGE_NETWORK_ADDED","CLUSTER_CHANGE_NETWORK_DELETED","CLUSTER_CHANGE_NETWORK_PROPERTY","CLUSTER_CHANGE_NETWORK_STATE","CLUSTER_CHANGE_NODE_ADDED","CLUSTER_CHANGE_NODE_DELETED","CLUSTER_CHANGE_NODE_PROPERTY","CLUSTER_CHANGE_NODE_STATE","CLUSTER_CHANGE_QUORUM_STATE","CLUSTER_CHANGE_REGISTRY_ATTRIBUTES","CLUSTER_CHANGE_REGISTRY_NAME","CLUSTER_CHANGE_REGISTRY_SUBTREE","CLUSTER_CHANGE_REGISTRY_VALUE","CLUSTER_CHANGE_RESOURCE_ADDED","CLUSTER_CHANGE_RESOURCE_DELETED","CLUSTER_CHANGE_RESOURCE_PROPERTY","CLUSTER_CHANGE_RESOURCE_STATE","CLUSTER_CHANGE_RESOURCE_TYPE_ADDED","CLUSTER_CHANGE_RESOURCE_TYPE_DELETED","CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY","CreateClusterNotifyPort","CreateClusterNotifyPort function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT","PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT function [Failover Cluster]","_wolf_createclusternotifyport","clusapi/CreateClusterNotifyPort","clusapi/PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT","mscs.createclusternotifyport"]
old-location: mscs\createclusternotifyport.htm
tech.root: MsCS
ms.assetid: 90e85f5d-54b4-48a5-bb5b-e46eb14781bb
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_CLUSTER_PROPERTY, CLUSTER_CHANGE_CLUSTER_RECONNECT, CLUSTER_CHANGE_CLUSTER_STATE, CLUSTER_CHANGE_GROUP_ADDED, CLUSTER_CHANGE_GROUP_DELETED, CLUSTER_CHANGE_GROUP_PROPERTY, CLUSTER_CHANGE_GROUP_STATE, CLUSTER_CHANGE_HANDLE_CLOSE, CLUSTER_CHANGE_NETINTERFACE_ADDED, CLUSTER_CHANGE_NETINTERFACE_DELETED, CLUSTER_CHANGE_NETINTERFACE_PROPERTY, CLUSTER_CHANGE_NETINTERFACE_STATE, CLUSTER_CHANGE_NETWORK_ADDED, CLUSTER_CHANGE_NETWORK_DELETED, CLUSTER_CHANGE_NETWORK_PROPERTY, CLUSTER_CHANGE_NETWORK_STATE, CLUSTER_CHANGE_NODE_ADDED, CLUSTER_CHANGE_NODE_DELETED, CLUSTER_CHANGE_NODE_PROPERTY, CLUSTER_CHANGE_NODE_STATE, CLUSTER_CHANGE_QUORUM_STATE, CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, CLUSTER_CHANGE_REGISTRY_NAME, CLUSTER_CHANGE_REGISTRY_SUBTREE, CLUSTER_CHANGE_REGISTRY_VALUE, CLUSTER_CHANGE_RESOURCE_ADDED, CLUSTER_CHANGE_RESOURCE_DELETED, CLUSTER_CHANGE_RESOURCE_PROPERTY, CLUSTER_CHANGE_RESOURCE_STATE, CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, CreateClusterNotifyPort, CreateClusterNotifyPort function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT, PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT function [Failover Cluster], _wolf_createclusternotifyport, clusapi/CreateClusterNotifyPort, clusapi/PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT, mscs.createclusternotifyport
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
 - CreateClusterNotifyPort
 - clusapi/CreateClusterNotifyPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ClusAPI.dll
api_name:
 - CreateClusterNotifyPort
---

# CreateClusterNotifyPort function


## -description

Creates 
    or modifies a notification port. For information on notification ports, see 
    <a href="/previous-versions/windows/desktop/mscs/receiving-cluster-events">Receiving Cluster Events</a>. The <b>PCLUSAPI_CREATE_CLUSTER_NOTIFY_PORT</b> type defines a pointer to this function.

## -parameters

### -param hChange [in]

Handle to a notification port or <b>INVALID_HANDLE_VALUE</b>, indicating that a new handle 
       should be created. If <i>hChange</i> is an existing handle, the events specified in 
       <i>dwFilter</i> are added to the notification port.

### -param hCluster [in]

Handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> to be associated with the 
       notification port identified by <i>hChange</i>, or 
       <b>INVALID_HANDLE_VALUE</b>, indicating that the notification port should not be associated 
       with a cluster. If <i>hChange</i> is not set to 
       <b>INVALID_HANDLE_VALUE</b>, <i>hCluster</i> cannot be set to 
       <b>INVALID_HANDLE_VALUE</b>.

### -param dwFilter [in]

Bitmask of flags enumerated from the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_change">CLUSTER_CHANGE</a> 
       enumeration that specifies the events that will cause notifications to be stored in the queue. One or more of 
       the following flags can be set using the OR operator, or you can specify all of the flags by using the value 
       <b>CLUSTER_CHANGE_ALL</b>.



#### CLUSTER_CHANGE_CLUSTER_PROPERTY (0x40000000)

The queue receives a notification when the cluster's properties change.



#### CLUSTER_CHANGE_CLUSTER_RECONNECT (0x00080000)

The queue receives a notification when the connection to the cluster identified by 
         <i>hCluster</i> is reestablished after a brief disconnect. Some events generated 
         immediately before or after this event may have been lost. You need to close all open connections and 
         reconnect to receive accurate state information.



#### CLUSTER_CHANGE_CLUSTER_STATE (0x20000000)

The queue receives a notification when the cluster becomes unavailable, meaning that all attempts to 
         communicate with the cluster fail.



#### CLUSTER_CHANGE_GROUP_ADDED (0x00004000)

The queue receives a notification when a new <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is 
         created in the cluster.



#### CLUSTER_CHANGE_GROUP_DELETED (0x00002000)

The queue receives a notification when an existing group is deleted.



#### CLUSTER_CHANGE_GROUP_PROPERTY (0x00008000)

The queue receives a notification when the 
         <a href="/previous-versions/windows/desktop/mscs/group-common-properties">properties</a> of a group change or when a 
         <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is added or removed from a group.



#### CLUSTER_CHANGE_GROUP_STATE (0x00001000)

The queue receives a notification when a group changes state. For a list of the possible group state 
         values, see <a href="/windows/desktop/api/clusapi/nf-clusapi-getclustergroupstate">GetClusterGroupState</a>.



#### CLUSTER_CHANGE_HANDLE_CLOSE (0x80000000)

The queue receives a notification when a handle associated with a 
         <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a> is closed.



#### CLUSTER_CHANGE_NETINTERFACE_ADDED (0x04000000)

The queue receives a notification when a new 
         <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a> is added to a cluster 
         <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.



#### CLUSTER_CHANGE_NETINTERFACE_DELETED (0x02000000)

The queue receives a notification when a network interface is permanently removed from a cluster node.



#### CLUSTER_CHANGE_NETINTERFACE_PROPERTY (0x08000000)

The queue receives a notification when the 
         <a href="/previous-versions/windows/desktop/mscs/network-interface-common-properties">properties</a> of an existing network 
         interface change.



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

The queue receives a notification when the 
         <a href="/previous-versions/windows/desktop/mscs/network-common-properties">properties</a> of an existing network 
         change.



#### CLUSTER_CHANGE_NETWORK_STATE (0x00100000)

The queue receives a notification when a network changes state. For a list of the possible network state 
         values, see <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetworkstate">GetClusterNetworkState</a>.



#### CLUSTER_CHANGE_NODE_ADDED (0x00000004)

The queue receives a notification when a new <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> 
         is added to the cluster. A node can be added only when the Cluster service is initially installed on the 
         node.



#### CLUSTER_CHANGE_NODE_DELETED (0x00000002)

The queue receives a notification when a node is permanently removed from a cluster. A node can be 
         permanently deleted from an existing cluster with a call to the 
         <a href="/windows/desktop/api/clusapi/nf-clusapi-evictclusternode">EvictClusterNode</a> function.



#### CLUSTER_CHANGE_NODE_PROPERTY (0x00000008)

The queue receives a notification when the node's properties change.



#### CLUSTER_CHANGE_NODE_STATE (0x00000001)

The queue receives a notification when a node changes state. For a list of possible node state values, see 
         <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>.



#### CLUSTER_CHANGE_QUORUM_STATE (0x10000000)

This notification is reserved for future use.



#### CLUSTER_CHANGE_REGISTRY_ATTRIBUTES (0x00000020)

The queue receives a notification when a 
         <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key's attributes are changed. The 
         only currently defined cluster database key attribute is its security descriptor, which can be changed with 
         <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetkeysecurity">ClusterRegSetKeySecurity</a>.



#### CLUSTER_CHANGE_REGISTRY_NAME (0x00000010)

The queue receives a notification when the name of a cluster database key has changed.



#### CLUSTER_CHANGE_REGISTRY_SUBTREE (0x00000080)

Indicates that the other <b>CLUSTER_CHANGE_REGISTRY</b> events apply to the entire 
         cluster database. If this flag is not included, the events apply only to the specified key.



#### CLUSTER_CHANGE_REGISTRY_VALUE (0x00000040)

The queue receives a notification when a value of the specified cluster database key is changed or deleted. 
         Cluster database values can be changed with the 
         <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetvalue">ClusterRegSetValue</a> function and deleted with 
         the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregdeletevalue">ClusterRegDeleteValue</a> function.



#### CLUSTER_CHANGE_RESOURCE_ADDED (0x00000400)

The queue receives a notification when a new 
         <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is created in the cluster.



#### CLUSTER_CHANGE_RESOURCE_DELETED (0x00000200)

The queue receives a notification when a resource is deleted.



#### CLUSTER_CHANGE_RESOURCE_PROPERTY (0x00000800)

The queue receives a notification when the 
         <a href="/previous-versions/windows/desktop/mscs/resource-common-properties">properties</a>, 
         <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a>, or 
         <a href="/previous-versions/windows/desktop/mscs/p-gly">possible owner</a> nodes of a resource change.



#### CLUSTER_CHANGE_RESOURCE_STATE (0x00000100)

The queue receives a notification when a resource changes state. For a list of the possible resource state 
         values, see <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcestate">GetClusterResourceState</a>.



#### CLUSTER_CHANGE_RESOURCE_TYPE_ADDED (0x00020000)

The queue receives a notification when a new 
         <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> is created in the cluster.



#### CLUSTER_CHANGE_RESOURCE_TYPE_DELETED (0x00010000)

The queue receives a notification when an existing resource type is deleted.



#### CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY (0x00040000)

The queue receives a notification when the 
         <a href="/previous-versions/windows/desktop/mscs/resource-common-properties">properties</a> of a resource type 
         change.

### -param dwNotifyKey [in]

A user-specified value to be associated with retrieving notifications from the notification port. The 
       <i>dwNotifyKey</i> is returned from 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a> when an event of one of the types 
       specified in <i>dwFilter</i> occurs.

## -returns

If the operation succeeds, the function returns a notification port handle.

If the operation fails, the 
       function returns <b>NULL</b>. For more information about the error, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information on using the 
     <b>CreateClusterNotifyPort</b>, 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a>, and 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-registerclusternotify">RegisterClusterNotify</a>, functions, see 
     <a href="/previous-versions/windows/desktop/mscs/receiving-cluster-events">Receiving Cluster Events</a>.


#### Examples

See the <a href="/previous-versions/windows/desktop/mscs/notification-port-example">Notification Port Example</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_change">CLUSTER_CHANGE</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternotifyport">CloseClusterNotifyPort</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclustergroupstate">GetClusterGroupState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetinterfacestate">GetClusterNetInterfaceState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetworkstate">GetClusterNetworkState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternotify">GetClusterNotify</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcestate">GetClusterResourceState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-registerclusternotify">RegisterClusterNotify</a>