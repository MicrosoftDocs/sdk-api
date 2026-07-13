---
UID: NF:clusapi.GetClusterNotify
title: GetClusterNotify function (clusapi.h)
description: Information relating to the next notification event that is stored for a notification port.
helpviewer_keywords: ["CLUSTER_CHANGE_CLUSTER_PROPERTY","CLUSTER_CHANGE_CLUSTER_RECONNECT","CLUSTER_CHANGE_CLUSTER_STATE","CLUSTER_CHANGE_GROUP_ADDED","CLUSTER_CHANGE_GROUP_DELETED","CLUSTER_CHANGE_GROUP_PROPERTY","CLUSTER_CHANGE_GROUP_STATE","CLUSTER_CHANGE_HANDLE_CLOSE","CLUSTER_CHANGE_NETINTERFACE_ADDED","CLUSTER_CHANGE_NETINTERFACE_DELETED","CLUSTER_CHANGE_NETINTERFACE_PROPERTY","CLUSTER_CHANGE_NETINTERFACE_STATE","CLUSTER_CHANGE_NETWORK_ADDED","CLUSTER_CHANGE_NETWORK_DELETED","CLUSTER_CHANGE_NETWORK_PROPERTY","CLUSTER_CHANGE_NETWORK_STATE","CLUSTER_CHANGE_NODE_ADDED","CLUSTER_CHANGE_NODE_DELETED","CLUSTER_CHANGE_NODE_PROPERTY","CLUSTER_CHANGE_NODE_STATE","CLUSTER_CHANGE_QUORUM_STATE","CLUSTER_CHANGE_REGISTRY_ATTRIBUTES","CLUSTER_CHANGE_REGISTRY_NAME","CLUSTER_CHANGE_REGISTRY_SUBTREE","CLUSTER_CHANGE_REGISTRY_VALUE","CLUSTER_CHANGE_RESOURCE_ADDED","CLUSTER_CHANGE_RESOURCE_DELETED","CLUSTER_CHANGE_RESOURCE_PROPERTY","CLUSTER_CHANGE_RESOURCE_STATE","CLUSTER_CHANGE_RESOURCE_TYPE_ADDED","CLUSTER_CHANGE_RESOURCE_TYPE_DELETED","CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY","GetClusterNotify","GetClusterNotify function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NOTIFY","PCLUSAPI_GET_CLUSTER_NOTIFY function [Failover Cluster]","_wolf_getclusternotify","clusapi/GetClusterNotify","clusapi/PCLUSAPI_GET_CLUSTER_NOTIFY","mscs.getclusternotify"]
old-location: mscs\getclusternotify.htm
tech.root: MsCS
ms.assetid: 9f650e2e-0651-4d1c-9314-b83f4f805f04
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_CLUSTER_PROPERTY, CLUSTER_CHANGE_CLUSTER_RECONNECT, CLUSTER_CHANGE_CLUSTER_STATE, CLUSTER_CHANGE_GROUP_ADDED, CLUSTER_CHANGE_GROUP_DELETED, CLUSTER_CHANGE_GROUP_PROPERTY, CLUSTER_CHANGE_GROUP_STATE, CLUSTER_CHANGE_HANDLE_CLOSE, CLUSTER_CHANGE_NETINTERFACE_ADDED, CLUSTER_CHANGE_NETINTERFACE_DELETED, CLUSTER_CHANGE_NETINTERFACE_PROPERTY, CLUSTER_CHANGE_NETINTERFACE_STATE, CLUSTER_CHANGE_NETWORK_ADDED, CLUSTER_CHANGE_NETWORK_DELETED, CLUSTER_CHANGE_NETWORK_PROPERTY, CLUSTER_CHANGE_NETWORK_STATE, CLUSTER_CHANGE_NODE_ADDED, CLUSTER_CHANGE_NODE_DELETED, CLUSTER_CHANGE_NODE_PROPERTY, CLUSTER_CHANGE_NODE_STATE, CLUSTER_CHANGE_QUORUM_STATE, CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, CLUSTER_CHANGE_REGISTRY_NAME, CLUSTER_CHANGE_REGISTRY_SUBTREE, CLUSTER_CHANGE_REGISTRY_VALUE, CLUSTER_CHANGE_RESOURCE_ADDED, CLUSTER_CHANGE_RESOURCE_DELETED, CLUSTER_CHANGE_RESOURCE_PROPERTY, CLUSTER_CHANGE_RESOURCE_STATE, CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, GetClusterNotify, GetClusterNotify function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NOTIFY, PCLUSAPI_GET_CLUSTER_NOTIFY function [Failover Cluster], _wolf_getclusternotify, clusapi/GetClusterNotify, clusapi/PCLUSAPI_GET_CLUSTER_NOTIFY, mscs.getclusternotify
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
 - GetClusterNotify
 - clusapi/GetClusterNotify
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
 - GetClusterNotify
---

# GetClusterNotify function


## -description

Returns information 
    relating to the next notification event that is  stored for a notification port. The <b>PCLUSAPI_GET_CLUSTER_NOTIFY</b> type defines a pointer to this function.

## -parameters

### -param hChange [in]

The handle to a notification port that is created with the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a> function.

### -param lpdwNotifyKey [out]

A  pointer to the notification key for the port that is  identified by the  <i>hChange</i> parameter.

### -param lpdwFilterType [out]

A pointer to a flag that indicates  the type of returned event. This flag is one of the following values from the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_change">CLUSTER_CHANGE</a> enumeration.



#### CLUSTER_CHANGE_CLUSTER_PROPERTY (0x40000000)

The queue receives a notification when the cluster's prioritized list of internal 
         <a href="/previous-versions/windows/desktop/mscs/networks">networks</a> changes.



#### CLUSTER_CHANGE_CLUSTER_RECONNECT (0x00080000)

The queue receives a notification when the connection to the cluster identified by the  
         <i>hCluster</i> parameter is reestablished after a brief disconnect. Some events generated 
         immediately before or after this event might  have been lost. You have to close all open connections and 
         reconnect to receive accurate state information.



#### CLUSTER_CHANGE_CLUSTER_STATE (0x20000000)

The queue receives a notification when the cluster becomes unavailable, meaning that all attempts to 
         communicate with the cluster fail.



#### CLUSTER_CHANGE_GROUP_ADDED (0x00004000)

The queue receives a notification when a new <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is created 
         in the cluster.



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

The queue receives a notification when a network interface is permanently removed from a cluster 
         node.



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

This notification is reserved for future use.



#### CLUSTER_CHANGE_NODE_STATE (0x00000001)

The queue receives a notification when a node changes state. For a list of possible node state values, see 
         <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>.



#### CLUSTER_CHANGE_QUORUM_STATE (0x10000000)

This notification is reserved for future use.



#### CLUSTER_CHANGE_REGISTRY_ATTRIBUTES (0x00000020)

The queue receives a notification when the attributes of  a 
         <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key  are changed. The 
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

### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the 
       <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a> that triggered the event. The 
       following list describes the content of <i>lpszName</i> by event type. Note that 
       <b>CLUSTER_CHANGE_REGISTRY_SUBTREE</b> is not included in the table; this event type is 
       never handled by <b>GetClusterNotify</b>.



#### CLUSTER_CHANGE_CLUSTER_PROPERTY (0x40000000)

Name of the changed cluster.



#### CLUSTER_CHANGE_CLUSTER_RECONNECT (0x00080000)

Name of the disconnected cluster.



#### CLUSTER_CHANGE_CLUSTER_STATE (0x20000000)

Name of the changed cluster.



#### CLUSTER_CHANGE_GROUP_ADDED (0x00004000)

New <a href="/previous-versions/windows/desktop/mscs/groups">group</a> name.



#### CLUSTER_CHANGE_GROUP_DELETED (0x00002000)

Deleted group name.



#### CLUSTER_CHANGE_GROUP_PROPERTY (0x00008000)

Name of the changed group.



#### CLUSTER_CHANGE_GROUP_STATE (0x00001000)

Name of the changed group.



#### CLUSTER_CHANGE_HANDLE_CLOSE (0x80000000)

Name of the object that is being closed.



#### CLUSTER_CHANGE_NODE_ADDED (0x00000004)

Name of new <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.



#### CLUSTER_CHANGE_NODE_DELETED (0x00000002)

Name of the deleted node.



#### CLUSTER_CHANGE_NODE_PROPERTY (0x00000008)

Name of the changed node.



#### CLUSTER_CHANGE_NODE_STATE (0x00000001)

Name of the changed node.



#### CLUSTER_CHANGE_REGISTRY_ATTRIBUTES (0x00000020)

Relative name of the changed 
         <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.



#### CLUSTER_CHANGE_REGISTRY_NAME (0x00000010)

Relative name of the changed cluster database key.



#### CLUSTER_CHANGE_REGISTRY_VALUE (0x00000040)

Relative name of the changed cluster database key.



#### CLUSTER_CHANGE_RESOURCE_ADDED (0x00000400)

New <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> name.



#### CLUSTER_CHANGE_RESOURCE_DELETED (0x00000200)

Deleted resource name.



#### CLUSTER_CHANGE_RESOURCE_PROPERTY (0x00000800)

Name of the changed resource.



#### CLUSTER_CHANGE_RESOURCE_STATE (0x00000100)

Name of the changed resource.



#### CLUSTER_CHANGE_RESOURCE_TYPE_ADDED (0x00020000)

Name of new <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>.



#### CLUSTER_CHANGE_RESOURCE_TYPE_DELETED (0x00010000)

Name of the deleted resource type.

### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters that the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

### -param dwMilliseconds [in, optional]

Optional time-out value that specifies how long the caller is willing to wait for the notification.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible 
       values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The handle that is represented in the <i>hChange</i> parameter is invalid or has been closed by 
         another thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
<dt>258 (0x102)</dt>
</dl>
</td>
<td width="60%">
The call timed out before the notification could be successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the  <i>lpszName</i>   parameter is not big enough to hold the result. The 
         <i>lpcchName</i>  parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Note that the <i>lpcchName</i> parameter refers to a count of characters and not a count of 
     bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. 
     For more information on sizing buffers, see 
     <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

The notifications are asynchronous, and the state of the cluster at the time that the application processes the 
     notification can be different than the state of the cluster at the time the notification was generated.


#### Examples

See the <a href="/previous-versions/windows/desktop/mscs/notification-port-example">Notification Port Example</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_change">CLUSTER_CHANGE</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternotifyport">CloseClusterNotifyPort</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusternotifyport">CreateClusterNotifyPort</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-registerclusternotify">RegisterClusterNotify</a>