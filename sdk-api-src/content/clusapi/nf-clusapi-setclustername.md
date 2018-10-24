---
UID: NF:clusapi.SetClusterName
title: SetClusterName function
author: windows-sdk-content
description: Sets the name for a cluster.
old-location: mscs\setclustername.htm
tech.root: mscs
ms.assetid: fac59879-d73c-4955-8454-a2e9d185da10
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PCLUSAPI_SetClusterName, PCLUSAPI_SetClusterName function [Failover Cluster], SetClusterName, SetClusterName function [Failover Cluster], _wolf_setclustername, clusapi/PCLUSAPI_SetClusterName, clusapi/SetClusterName, mscs.setclustername
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - SetClusterName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterName function


## -description


Sets the name for a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_SetClusterName</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster to rename.


### -param lpszNewClusterName [in]

Pointer to a null-terminated Unicode string containing the new cluster name.


## -returns



If the operation succeeds, the function returns <b>ERROR_RESOURCE_PROPERTIES_STORED</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The cluster name is stored in the  <a href="https://msdn.microsoft.com/en-us/library/Aa371735(v=VS.85).aspx">Name</a> private property of the core  <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource (that is, the Network Name resource of the cluster). Because of possible dependencies on this resource, the change is not effective until the Network Name resource is brought back online.

Do not call  <b>SetClusterName</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371735(v=VS.85).aspx">Name</a>
 

 

