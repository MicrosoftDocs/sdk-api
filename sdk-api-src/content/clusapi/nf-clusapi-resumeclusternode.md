---
UID: NF:clusapi.ResumeClusterNode
title: ResumeClusterNode function
author: windows-sdk-content
description: Requests that a paused node resume its cluster activity. The PCLUSAPI_RESUME_CLUSTER_NODE type defines a pointer to this function.
old-location: mscs\resumeclusternode.htm
tech.root: mscs
ms.assetid: 01b98d8d-9235-4133-aa3c-f9ad45be8aaf
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PCLUSAPI_RESUME_CLUSTER_NODE, PCLUSAPI_RESUME_CLUSTER_NODE function [Failover Cluster], ResumeClusterNode, ResumeClusterNode function [Failover Cluster], _wolf_resumeclusternode, clusapi/PCLUSAPI_RESUME_CLUSTER_NODE, clusapi/ResumeClusterNode, mscs.resumeclusternode
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
 - ResumeClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResumeClusterNode function


## -description


Requests that a paused  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> resume its <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> activity. The <b>PCLUSAPI_RESUME_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the paused node.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a>
 

 

