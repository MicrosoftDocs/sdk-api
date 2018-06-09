---
UID: NC:clusapi.PCLUSAPI_SetClusterName
title: PCLUSAPI_SetClusterName
author: windows-sdk-content
description: Sets the name for a cluster.
old-location: mscs\setclustername.htm
old-project: MsCS
ms.assetid: fac59879-d73c-4955-8454-a2e9d185da10
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PCLUSAPI_SetClusterName, PCLUSAPI_SetClusterName callback, PCLUSAPI_SetClusterName callback function [Failover Cluster], _wolf_setclustername, clusapi/PCLUSAPI_SetClusterName, mscs.setclustername
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_SetClusterName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SetClusterName callback function


## -description


Sets the name for a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The <b>PCLUSAPI_SetClusterName</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster to rename.


### -param lpszNewClusterName [in]

Pointer to a null-terminated Unicode string containing the new cluster name.


## -returns



If the operation succeeds, the function returns <b>ERROR_RESOURCE_PROPERTIES_STORED</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The cluster name is stored in the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> private property of the core  <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource (that is, the Network Name resource of the cluster). Because of possible dependencies on this resource, the change is not effective until the Network Name resource is brought back online.

Do not call  <i>SetClusterName</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
 

 

