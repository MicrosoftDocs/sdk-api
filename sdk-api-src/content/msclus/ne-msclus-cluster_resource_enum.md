---
UID: NE:msclus.CLUSTER_RESOURCE_ENUM
title: CLUSTER_RESOURCE_ENUM
author: windows-sdk-content
description: Describes the type of cluster object being enumerated by the ClusterResourceEnum or ClusterResourceOpenEnum functions.
old-location: mscs\cluster_resource_enum.htm
tech.root: mscs
ms.assetid: 8b59ab43-7e03-4ddf-82cc-9945e9da6462
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CLUSTER_RESOURCE_ENUM, CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster], CLUSTER_RESOURCE_ENUM_ALL, CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, _CLUSTER_RESOURCE_ENUM, _CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_ENUM, clusapi/CLUSTER_RESOURCE_ENUM_ALL, clusapi/CLUSTER_RESOURCE_ENUM_DEPENDS, clusapi/CLUSTER_RESOURCE_ENUM_NODES, clusapi/CLUSTER_RESOURCE_ENUM_PROVIDES, clusapi/_CLUSTER_RESOURCE_ENUM, msclus/CLUSTER_RESOURCE_ENUM, msclus/CLUSTER_RESOURCE_ENUM_ALL, msclus/CLUSTER_RESOURCE_ENUM_DEPENDS, msclus/CLUSTER_RESOURCE_ENUM_NODES, msclus/CLUSTER_RESOURCE_ENUM_PROVIDES, msclus/_CLUSTER_RESOURCE_ENUM, mscs.cluster_resource_enum
ms.prod: windows
ms.technology: windows-sdk
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
 - CLUSTER_RESOURCE_ENUM
product: Windows
targetos: Windows
req.typenames: CLUSTER_RESOURCE_ENUM
req.redist: 
---

# CLUSTER_RESOURCE_ENUM enumeration


## -description


Describes the type of cluster object being enumerated by the 
    <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> or 
    <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> 
    functions.


## -enum-fields




### -field CLUSTER_RESOURCE_ENUM_DEPENDS

A resource that the resource identified by the 
       <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> or 
       <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> functions directly 
       depends on.


### -field CLUSTER_RESOURCE_ENUM_PROVIDES

A resource that directly depends on the resource identified by the 
       <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> or 
       <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> functions.


### -field CLUSTER_RESOURCE_ENUM_NODES

A node that can host the resource identified by the 
       <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> or 
       <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> functions.


### -field CLUSTER_RESOURCE_ENUM_ALL

All nodes and resources identified by the 
       <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> or 
       <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> functions.


## -see-also




<a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a>



<a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

