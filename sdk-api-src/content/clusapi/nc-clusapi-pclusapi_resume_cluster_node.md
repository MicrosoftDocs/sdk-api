---
UID: NC:clusapi.PCLUSAPI_RESUME_CLUSTER_NODE
title: PCLUSAPI_RESUME_CLUSTER_NODE
author: windows-sdk-content
description: Requests that a paused node resume its cluster activity. The PCLUSAPI_RESUME_CLUSTER_NODE type defines a pointer to this function.
old-location: mscs\resumeclusternode.htm
old-project: MsCS
ms.assetid: 01b98d8d-9235-4133-aa3c-f9ad45be8aaf
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_RESUME_CLUSTER_NODE, PCLUSAPI_RESUME_CLUSTER_NODE callback, PCLUSAPI_RESUME_CLUSTER_NODE callback function [Failover Cluster], _wolf_resumeclusternode, clusapi/PCLUSAPI_RESUME_CLUSTER_NODE, mscs.resumeclusternode
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_RESUME_CLUSTER_NODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_RESUME_CLUSTER_NODE callback function


## -description


Requests that a paused  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> resume its <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> activity. The <b>PCLUSAPI_RESUME_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the paused node.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a>
 

 

