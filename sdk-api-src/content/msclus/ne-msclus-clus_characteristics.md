---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CLUS_CHARACTERISTICS enumeration


## -description


Enumerates characteristics of resource types and resources.


## -enum-fields




### -field CLUS_CHAR_UNKNOWN

Resources of this type have no known characteristics.


### -field CLUS_CHAR_QUORUM

Resources of this type are capable of being the 
       <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource type</a> for a cluster.


### -field CLUS_CHAR_DELETE_REQUIRES_ALL_NODES

Resources of this type cannot be deleted unless all nodes are active.


### -field CLUS_CHAR_LOCAL_QUORUM

Not supported.


### -field CLUS_CHAR_LOCAL_QUORUM_DEBUG

Not supported.


### -field CLUS_CHAR_REQUIRES_STATE_CHANGE_REASON

The <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> will receive the 
       <a href="https://msdn.microsoft.com/3261c8eb-b88b-428a-8a2b-684e0967f9de">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
       control code.


### -field CLUS_CHAR_BROADCAST_DELETE

Not supported.


### -field CLUS_CHAR_SINGLE_CLUSTER_INSTANCE

Only one instance of this resource type is allowed in a cluster.


### -field CLUS_CHAR_SINGLE_GROUP_INSTANCE

Only one instance of this resource type is allowed in a group.


### -field CLUS_CHAR_COEXIST_IN_SHARED_VOLUME_GROUP

The resource can be made part of a special group. Protocol version 2.0 servers do not support this value.


### -field CLUS_CHAR_PLACEMENT_DATA

The resource type can be queried to get more information about how many resources it uses. For example, in the <a href="https://msdn.microsoft.com/9f1dcda8-f34b-4801-a35a-970c04ddd6b8">virtual machine</a> resource type, information is returned about how much memory is required for the virtual machine to be started.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.


### -field CLUS_CHAR_MONITOR_DETACH

The resource can be deleted without being taken offline. Protocol version 2.0 servers do not support this value.




### -field CLUS_CHAR_MONITOR_REATTACH

This value is reserved for local use and must be ignored by the client. Protocol version 2.0 servers do not support this value.


### -field CLUS_CHAR_OPERATION_CONTEXT

This value is reserved for local use and must be ignored by the client. Protocol version 2.0 servers do not support this value.


### -field CLUS_CHAR_CLONES

This value is reserved for local use and must be ignored by the client. Protocol version 2.0 servers do not support this value.


### -field CLUS_CHAR_NOT_PREEMPTABLE

The resource should not be preempted, even if the whole group is being preempted.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.


### -field CLUS_CHAR_NOTIFY_NEW_OWNER

The resource can receive a new owner.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012 R2.


### -field CLUS_CHAR_SUPPORTS_UNMONITORED_STATE

The resource can continue run in an unmonitored state when it losses cluster membership.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2016.


### -field CLUS_CHAR_INFRASTRUCTURE

This value is reserved for infrastructure.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2016.


## -see-also




<a href="https://msdn.microsoft.com/e01103a4-b527-4b8b-9933-7dbe0e6f2ddd">CLUSCTL_GROUP_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/5ead5c71-0a35-44c3-aa77-c7c4b8bb197b">CLUSCTL_NETINTERFACE_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/a1777dd3-656b-473a-a5a0-4fd9de6c0575">CLUSCTL_NETWORK_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/8979b006-5494-4587-9675-983ee9021273">CLUSCTL_NODE_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/02de0119-76af-445f-b107-f0ffa57e5ade">CLUSCTL_RESOURCE_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/d968810f-cd95-43a8-8897-43ebf0bd6f08">CLUSCTL_RESOURCE_TYPE_GET_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

