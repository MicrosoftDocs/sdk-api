---
UID: NE:clusapi.CLUSTER_RESOURCE_CREATE_FLAGS
title: CLUSTER_RESOURCE_CREATE_FLAGS
author: windows-sdk-content
description: Determines which resource monitor a given resource will be assigned to.
old-location: mscs\cluster_resource_create_flags.htm
tech.root: MsCS
ms.assetid: 16f5ab58-2507-431a-98f9-bd00a24485ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CLUSTER_RESOURCE_CREATE_FLAGS, CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, CLUSTER_RESOURCE_VALID_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_CREATE_FLAGS, clusapi/CLUSTER_RESOURCE_DEFAULT_MONITOR, clusapi/CLUSTER_RESOURCE_SEPARATE_MONITOR, clusapi/CLUSTER_RESOURCE_VALID_FLAGS, clusapi/_CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_DEFAULT_MONITOR, msclus/CLUSTER_RESOURCE_SEPARATE_MONITOR, msclus/CLUSTER_RESOURCE_VALID_FLAGS, msclus/_CLUSTER_RESOURCE_CREATE_FLAGS, mscs.cluster_resource_create_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - CLUSTER_RESOURCE_CREATE_FLAGS
product: Windows
targetos: Windows
req.typenames: CLUSTER_RESOURCE_CREATE_FLAGS
req.redist: 
---

# CLUSTER_RESOURCE_CREATE_FLAGS enumeration


## -description


Determines which resource monitor a given resource will be assigned to.


## -enum-fields




### -field CLUSTER_RESOURCE_DEFAULT_MONITOR

The <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> determines the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa372266(v=VS.85).aspx">Resource Monitor</a> to which the new resource will be 
      assigned.


### -field CLUSTER_RESOURCE_SEPARATE_MONITOR

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
      resource.


### -field CLUSTER_RESOURCE_VALID_FLAGS

Contains all valid flags for the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb309165(v=VS.85).aspx">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.


## -see-also




<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368404(v=VS.85).aspx">CreateItem Method of the ClusResDependencies Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368423(v=VS.85).aspx">CreateItem Method of the ClusResDependents Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368804(v=VS.85).aspx">CreateItem Method of the ClusResTypeResources Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368727(v=VS.85).aspx">CreateItem Method of the ClusResources Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>
 

 

