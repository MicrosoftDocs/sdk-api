---
UID: NE:clusapi.CLUSTER_CHANGE
title: CLUSTER_CHANGE
author: windows-sdk-content
description: Describes the type of notification returned.
old-location: mscs\cluster_change.htm
tech.root: mscs
ms.assetid: d396d490-84d0-4bf8-9c0d-8597b3baf0ec
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CLUSTER_CHANGE, CLUSTER_CHANGE enumeration [Failover Cluster], CLUSTER_CHANGE_ALL, CLUSTER_CHANGE_CLUSTER_PROPERTY, CLUSTER_CHANGE_CLUSTER_RECONNECT, CLUSTER_CHANGE_CLUSTER_STATE, CLUSTER_CHANGE_GROUP_ADDED, CLUSTER_CHANGE_GROUP_DELETED, CLUSTER_CHANGE_GROUP_PROPERTY, CLUSTER_CHANGE_GROUP_STATE, CLUSTER_CHANGE_HANDLE_CLOSE, CLUSTER_CHANGE_NETINTERFACE_ADDED, CLUSTER_CHANGE_NETINTERFACE_DELETED, CLUSTER_CHANGE_NETINTERFACE_PROPERTY, CLUSTER_CHANGE_NETINTERFACE_STATE, CLUSTER_CHANGE_NETWORK_ADDED, CLUSTER_CHANGE_NETWORK_DELETED, CLUSTER_CHANGE_NETWORK_PROPERTY, CLUSTER_CHANGE_NETWORK_STATE, CLUSTER_CHANGE_NODE_ADDED, CLUSTER_CHANGE_NODE_DELETED, CLUSTER_CHANGE_NODE_PROPERTY, CLUSTER_CHANGE_NODE_STATE, CLUSTER_CHANGE_QUORUM_STATE, CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, CLUSTER_CHANGE_REGISTRY_NAME, CLUSTER_CHANGE_REGISTRY_SUBTREE, CLUSTER_CHANGE_REGISTRY_VALUE, CLUSTER_CHANGE_RESOURCE_ADDED, CLUSTER_CHANGE_RESOURCE_DELETED, CLUSTER_CHANGE_RESOURCE_PROPERTY, CLUSTER_CHANGE_RESOURCE_STATE, CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, _CLUSTER_CHANGE, _CLUSTER_CHANGE enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE, clusapi/CLUSTER_CHANGE_ALL, clusapi/CLUSTER_CHANGE_CLUSTER_PROPERTY, clusapi/CLUSTER_CHANGE_CLUSTER_RECONNECT, clusapi/CLUSTER_CHANGE_CLUSTER_STATE, clusapi/CLUSTER_CHANGE_GROUP_ADDED, clusapi/CLUSTER_CHANGE_GROUP_DELETED, clusapi/CLUSTER_CHANGE_GROUP_PROPERTY, clusapi/CLUSTER_CHANGE_GROUP_STATE, clusapi/CLUSTER_CHANGE_HANDLE_CLOSE, clusapi/CLUSTER_CHANGE_NETINTERFACE_ADDED, clusapi/CLUSTER_CHANGE_NETINTERFACE_DELETED, clusapi/CLUSTER_CHANGE_NETINTERFACE_PROPERTY, clusapi/CLUSTER_CHANGE_NETINTERFACE_STATE, clusapi/CLUSTER_CHANGE_NETWORK_ADDED, clusapi/CLUSTER_CHANGE_NETWORK_DELETED, clusapi/CLUSTER_CHANGE_NETWORK_PROPERTY, clusapi/CLUSTER_CHANGE_NETWORK_STATE, clusapi/CLUSTER_CHANGE_NODE_ADDED, clusapi/CLUSTER_CHANGE_NODE_DELETED, clusapi/CLUSTER_CHANGE_NODE_PROPERTY, clusapi/CLUSTER_CHANGE_NODE_STATE, clusapi/CLUSTER_CHANGE_QUORUM_STATE, clusapi/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, clusapi/CLUSTER_CHANGE_REGISTRY_NAME, clusapi/CLUSTER_CHANGE_REGISTRY_SUBTREE, clusapi/CLUSTER_CHANGE_REGISTRY_VALUE, clusapi/CLUSTER_CHANGE_RESOURCE_ADDED, clusapi/CLUSTER_CHANGE_RESOURCE_DELETED, clusapi/CLUSTER_CHANGE_RESOURCE_PROPERTY, clusapi/CLUSTER_CHANGE_RESOURCE_STATE, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, clusapi/_CLUSTER_CHANGE, msclus/CLUSTER_CHANGE, msclus/CLUSTER_CHANGE_ALL, msclus/CLUSTER_CHANGE_CLUSTER_PROPERTY, msclus/CLUSTER_CHANGE_CLUSTER_RECONNECT, msclus/CLUSTER_CHANGE_CLUSTER_STATE, msclus/CLUSTER_CHANGE_GROUP_ADDED, msclus/CLUSTER_CHANGE_GROUP_DELETED, msclus/CLUSTER_CHANGE_GROUP_PROPERTY, msclus/CLUSTER_CHANGE_GROUP_STATE, msclus/CLUSTER_CHANGE_HANDLE_CLOSE, msclus/CLUSTER_CHANGE_NETINTERFACE_ADDED, msclus/CLUSTER_CHANGE_NETINTERFACE_DELETED, msclus/CLUSTER_CHANGE_NETINTERFACE_PROPERTY, msclus/CLUSTER_CHANGE_NETINTERFACE_STATE, msclus/CLUSTER_CHANGE_NETWORK_ADDED, msclus/CLUSTER_CHANGE_NETWORK_DELETED, msclus/CLUSTER_CHANGE_NETWORK_PROPERTY, msclus/CLUSTER_CHANGE_NETWORK_STATE, msclus/CLUSTER_CHANGE_NODE_ADDED, msclus/CLUSTER_CHANGE_NODE_DELETED, msclus/CLUSTER_CHANGE_NODE_PROPERTY, msclus/CLUSTER_CHANGE_NODE_STATE, msclus/CLUSTER_CHANGE_QUORUM_STATE, msclus/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES, msclus/CLUSTER_CHANGE_REGISTRY_NAME, msclus/CLUSTER_CHANGE_REGISTRY_SUBTREE, msclus/CLUSTER_CHANGE_REGISTRY_VALUE, msclus/CLUSTER_CHANGE_RESOURCE_ADDED, msclus/CLUSTER_CHANGE_RESOURCE_DELETED, msclus/CLUSTER_CHANGE_RESOURCE_PROPERTY, msclus/CLUSTER_CHANGE_RESOURCE_STATE, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_ADDED, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY, msclus/_CLUSTER_CHANGE, mscs.cluster_change
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_CHANGE
product: Windows
targetos: Windows
req.typenames: CLUSTER_CHANGE
req.redist: 
---

# CLUSTER_CHANGE enumeration


## -description


Describes the type of notification returned. The 
    <a href="https://msdn.microsoft.com/9f650e2e-0651-4d1c-9314-b83f4f805f04">GetClusterNotify</a>, 
    <a href="https://msdn.microsoft.com/ddf0e01c-08e9-4e32-b012-76c8a41037a7">RegisterClusterNotify</a>, and 
    <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> functions use this enumeration.


## -enum-fields




### -field CLUSTER_CHANGE_NODE_STATE

The queue receives a notification when a node changes state. For a list of possible node state values, see 
       <a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a>.


### -field CLUSTER_CHANGE_NODE_DELETED

The queue receives a notification when a node is permanently removed from a cluster. A node can be 
       permanently deleted from an existing cluster with a call to the 
       <a href="https://msdn.microsoft.com/0353b640-5fa6-4e83-a7e5-1b4bd2ca16d9">EvictClusterNode</a> function.


### -field CLUSTER_CHANGE_NODE_ADDED

The queue receives a notification when a new <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> 
       is added to the cluster. A node can be added only when the Cluster service is initially installed on the 
       node.


### -field CLUSTER_CHANGE_NODE_PROPERTY

This notification is reserved for future use.


### -field CLUSTER_CHANGE_REGISTRY_NAME

The queue receives a notification when the name of a cluster database key has changed.


### -field CLUSTER_CHANGE_REGISTRY_ATTRIBUTES

The queue receives a notification when a 
       <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key's attributes are changed. The only 
       currently defined cluster database key attribute is its security descriptor, which can be changed with 
       <a href="https://msdn.microsoft.com/adb2ea52-6a3a-4243-944d-c7ae68a42a1a">ClusterRegSetKeySecurity</a>.


### -field CLUSTER_CHANGE_REGISTRY_VALUE

The queue receives a notification when a value of the specified cluster database key is changed or deleted. 
       Cluster database values can be changed with the 
       <a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a> function and deleted with the 
       <a href="https://msdn.microsoft.com/81d2936e-6f2c-48d9-b898-c1d8b2c946e6">ClusterRegDeleteValue</a> function.


### -field CLUSTER_CHANGE_REGISTRY_SUBTREE

Indicates that the other <b>CLUSTER_CHANGE_REGISTRY_*</b> events apply to the entire 
       cluster database. If this flag is not included, the events apply only to the specified key.


### -field CLUSTER_CHANGE_RESOURCE_STATE

The queue receives a notification when a resource changes state. For a list of the possible resource state 
       values, see <a href="https://msdn.microsoft.com/c3897c96-743e-4753-8fef-b8defe4f2b00">GetClusterResourceState</a>.


### -field CLUSTER_CHANGE_RESOURCE_DELETED

The queue receives a notification when a resource is deleted.


### -field CLUSTER_CHANGE_RESOURCE_ADDED

The queue receives a notification when a new 
      <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> is created in the cluster.


### -field CLUSTER_CHANGE_RESOURCE_PROPERTY

The queue receives a notification when the 
       <a href="https://msdn.microsoft.com/b84fe8fe-a49e-4c3c-acbd-f9cfe5ac0782">properties</a>, 
       <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a>, or 
       <a href="p_gly.htm">possible owner</a> nodes of a resource change.


### -field CLUSTER_CHANGE_GROUP_STATE

The queue receives a notification when a group changes state. For a list of the possible group state 
       values, see <a href="https://msdn.microsoft.com/5f794dee-aeee-4906-ba63-c154bfda4d17">GetClusterGroupState</a>.


### -field CLUSTER_CHANGE_GROUP_DELETED

The queue receives a notification when an existing group is deleted.


### -field CLUSTER_CHANGE_GROUP_ADDED

The queue receives a notification when a new <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> is created 
       in the cluster.


### -field CLUSTER_CHANGE_GROUP_PROPERTY

The queue receives a notification when the 
       <a href="https://msdn.microsoft.com/bc13356c-06d8-400e-9fe0-3afbda4f228a">properties</a> of a group change or when a 
       <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> is added or removed from a group.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_DELETED

The queue receives a notification when an existing resource type is deleted.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_ADDED

The queue receives a notification when a new 
      <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> is created in the cluster.


### -field CLUSTER_CHANGE_RESOURCE_TYPE_PROPERTY

The queue receives a notification when the 
       <a href="https://msdn.microsoft.com/b84fe8fe-a49e-4c3c-acbd-f9cfe5ac0782">properties</a> of a resource type 
       change.


### -field CLUSTER_CHANGE_CLUSTER_RECONNECT

When generated by a client, this value indicates that the RPC connection to a server has been reconnected to another server for the specified cluster. When generated by the server, this value indicates that notification events were dropped by the server for the port.


### -field CLUSTER_CHANGE_NETWORK_STATE

The queue receives a notification when a network changes state. For a list of the possible network state 
       values, see <a href="https://msdn.microsoft.com/7fdbc0cf-fa7b-4b48-bd3c-46f174fc514a">GetClusterNetworkState</a>.


### -field CLUSTER_CHANGE_NETWORK_DELETED

The queue receives a notification when a network is permanently removed from the cluster environment.


### -field CLUSTER_CHANGE_NETWORK_ADDED

The queue receives a notification when a new 
       <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> is added to the cluster environment.


### -field CLUSTER_CHANGE_NETWORK_PROPERTY

The queue receives a notification when the 
       <a href="https://msdn.microsoft.com/9a59f372-0d09-4dba-adcf-38c7f2a8e006">properties</a> of an existing network change.


### -field CLUSTER_CHANGE_NETINTERFACE_STATE

The queue receives a notification when a network interface changes state. For a list of the possible network 
       interface state values, see 
       <a href="https://msdn.microsoft.com/d84a5e3f-d0f9-4345-b008-e15c277dcbd5">GetClusterNetInterfaceState</a>.


### -field CLUSTER_CHANGE_NETINTERFACE_DELETED

The queue receives a notification when a network interface is permanently removed from a cluster node.


### -field CLUSTER_CHANGE_NETINTERFACE_ADDED

The queue receives a notification when a new 
       <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a> is added to a cluster 
       <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


### -field CLUSTER_CHANGE_NETINTERFACE_PROPERTY

The queue receives a notification when the 
       <a href="https://msdn.microsoft.com/4641238d-4b9e-40c7-9d5e-751d69be1912">properties</a> of an existing network 
       interface change.


### -field CLUSTER_CHANGE_QUORUM_STATE

This notification is reserved for future use.


### -field CLUSTER_CHANGE_CLUSTER_STATE

The queue receives a notification when the cluster becomes unavailable, meaning that all attempts to 
       communicate with the cluster fail.


### -field CLUSTER_CHANGE_CLUSTER_PROPERTY

The queue receives a notification when the cluster's prioritized list of internal 
       <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> changes.


### -field CLUSTER_CHANGE_HANDLE_CLOSE

The queue receives a notification when a handle associated with a 
       <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a> is closed.


### -field CLUSTER_CHANGE_ALL


## -see-also




<a href="https://msdn.microsoft.com/adb2ea52-6a3a-4243-944d-c7ae68a42a1a">ClusterRegSetKeySecurity</a>



<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/9f650e2e-0651-4d1c-9314-b83f4f805f04">GetClusterNotify</a>



<a href="https://msdn.microsoft.com/ddf0e01c-08e9-4e32-b012-76c8a41037a7">RegisterClusterNotify</a>
 

 

