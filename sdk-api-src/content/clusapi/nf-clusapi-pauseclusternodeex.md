---
UID: NF:clusapi.PauseClusterNodeEx
title: PauseClusterNodeEx function (clusapi.h)
author: windows-sdk-content
description: Requests that a node temporarily suspends its cluster activity.
old-location: mscs\pauseclusternodeex.htm
tech.root: MsCS
ms.assetid: 632C26C2-ED12-40DC-9615-4A09A7E2F7CB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_PAUSE_CLUSTER_NODE_EX, PCLUSAPI_PAUSE_CLUSTER_NODE_EX function [Failover Cluster], PauseClusterNodeEx, PauseClusterNodeEx function [Failover Cluster], clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE_EX, clusapi/PauseClusterNodeEx, mscs.pauseclusternodeex
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - PauseClusterNodeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PauseClusterNodeEx function


## -description


Requests that a 
node temporarily suspends its cluster activity.


## -parameters




### -param hNode [in]

A handle to the node to suspend.


### -param bDrainNode [in]

<b>TRUE</b> to drain the node; otherwise <b>FALSE</b>.


### -param dwPauseFlags [in] [in]

TBD


### -param hNodeDrainTarget [in, optional] [in, optional]

TBD


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

