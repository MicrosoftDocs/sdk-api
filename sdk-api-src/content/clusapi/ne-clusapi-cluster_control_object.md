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

# CLUSTER_CONTROL_OBJECT enumeration


## -description


The 8-bit object component of a control code that indicates the type of cluster object to which the 
    control code applies. For more information, see 
    <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a>.


## -enum-fields




### -field CLUS_OBJECT_INVALID

Zero is not a valid object code value.


### -field CLUS_OBJECT_RESOURCE

Object code part of <a href="https://msdn.microsoft.com/71ec60fd-67ec-4932-983b-f78c6b552954">resource control codes</a> 
       that identifies cluster <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> as the target.


### -field CLUS_OBJECT_RESOURCE_TYPE

Object code part of 
       <a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">resource type control codes</a> that identifies 
       cluster <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> as the target.


### -field CLUS_OBJECT_GROUP

Object code part of 
       <a href="https://msdn.microsoft.com/41f93d49-c021-4fcb-9d38-f801702b9e51">group control codes</a> that identifies cluster 
        <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> as the target.


### -field CLUS_OBJECT_NODE

Object code part of <a href="https://msdn.microsoft.com/39b59726-e00e-4011-a7bc-96698e12f1e4">node control codes</a> that 
       identifies cluster <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> as the target.


### -field CLUS_OBJECT_NETWORK

Object code part of <a href="https://msdn.microsoft.com/e9156fc0-688c-4a5b-9c78-91668bf2bd40">network control codes</a> that 
       identifies cluster <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> as the target.


### -field CLUS_OBJECT_NETINTERFACE

Object code part of 
       <a href="https://msdn.microsoft.com/adc97081-e778-426d-8296-9dea9f22a4e4">network interface control codes</a> that 
       identifies cluster <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> as the 
       target.


### -field CLUS_OBJECT_CLUSTER

Object code part of <a href="https://msdn.microsoft.com/cabd9d59-7ace-4081-9de1-7645c882a64d">cluster control codes</a> that 
       identifies a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> as the target.


### -field CLUS_OBJECT_GROUPSET

Object code part of <a href="https://msdn.microsoft.com/cabd9d59-7ace-4081-9de1-7645c882a64d">cluster control codes</a> that 
       identifies a groupset as the target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This constant is not supported prior to Windows Server 2016.


### -field CLUS_OBJECT_USER

Object code part of <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control codes</a> that identifies 
       cluster object types not defined by Windows Clustering.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

