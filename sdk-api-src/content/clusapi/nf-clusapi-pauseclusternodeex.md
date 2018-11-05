---
UID: NF:clusapi.PauseClusterNodeEx
title: PauseClusterNodeEx function
author: windows-sdk-content
description: Requests that a node temporarily suspends its cluster activity.
old-location: mscs\pauseclusternodeex.htm
tech.root: mscs
ms.assetid: 632C26C2-ED12-40DC-9615-4A09A7E2F7CB
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PCLUSAPI_PAUSE_CLUSTER_NODE_EX, PCLUSAPI_PAUSE_CLUSTER_NODE_EX function [Failover Cluster], PauseClusterNodeEx, PauseClusterNodeEx function [Failover Cluster], clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE_EX, clusapi/PauseClusterNodeEx, mscs.pauseclusternodeex
ms.prod: windows-hardware
ms.technology: windows-devices
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
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>
 

 

