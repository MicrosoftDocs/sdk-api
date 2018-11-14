---
UID: NE:msclus.CLUSTER_CONTROL_OBJECT
title: CLUSTER_CONTROL_OBJECT
author: windows-sdk-content
description: The 8-bit object component of a control code that indicates the type of cluster object to which the control code applies. For more information, see Control Code Architecture.
old-location: mscs\cluster_control_object.htm
tech.root: mscs
ms.assetid: 63719776-0b3a-470a-a732-40e62064c6fc
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CLUSTER_CONTROL_OBJECT, CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster], CLUS_OBJECT_CLUSTER, CLUS_OBJECT_GROUP, CLUS_OBJECT_GROUPSET, CLUS_OBJECT_INVALID, CLUS_OBJECT_NETINTERFACE, CLUS_OBJECT_NETWORK, CLUS_OBJECT_NODE, CLUS_OBJECT_RESOURCE, CLUS_OBJECT_RESOURCE_TYPE, CLUS_OBJECT_USER, _CLUSTER_CONTROL_OBJECT, _CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster], clusapi/CLUSTER_CONTROL_OBJECT, clusapi/CLUS_OBJECT_CLUSTER, clusapi/CLUS_OBJECT_GROUP, clusapi/CLUS_OBJECT_GROUPSET, clusapi/CLUS_OBJECT_INVALID, clusapi/CLUS_OBJECT_NETINTERFACE, clusapi/CLUS_OBJECT_NETWORK, clusapi/CLUS_OBJECT_NODE, clusapi/CLUS_OBJECT_RESOURCE, clusapi/CLUS_OBJECT_RESOURCE_TYPE, clusapi/CLUS_OBJECT_USER, clusapi/_CLUSTER_CONTROL_OBJECT, msclus/CLUSTER_CONTROL_OBJECT, msclus/CLUS_OBJECT_CLUSTER, msclus/CLUS_OBJECT_GROUP, msclus/CLUS_OBJECT_GROUPSET, msclus/CLUS_OBJECT_INVALID, msclus/CLUS_OBJECT_NETINTERFACE, msclus/CLUS_OBJECT_NETWORK, msclus/CLUS_OBJECT_NODE, msclus/CLUS_OBJECT_RESOURCE, msclus/CLUS_OBJECT_RESOURCE_TYPE, msclus/CLUS_OBJECT_USER, msclus/_CLUSTER_CONTROL_OBJECT, mscs.cluster_control_object
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msclus.h
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
 - CLUSTER_CONTROL_OBJECT
product: Windows
targetos: Windows
req.typenames: CLUSTER_CONTROL_OBJECT
req.redist: 
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
       identifies a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> as the target.


### -field CLUS_OBJECT_GROUPSET

Object code part of <a href="https://msdn.microsoft.com/cabd9d59-7ace-4081-9de1-7645c882a64d">cluster control codes</a> that 
       identifies a groupset as the target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This constant is not supported prior to Windows Server 2016.


### -field CLUS_OBJECT_USER

Object code part of <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control codes</a> that identifies 
       cluster object types not defined by Windows Clustering.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

