---
UID: NF:clusapi.CloseClusterNode
title: CloseClusterNode function
author: windows-sdk-content
description: Closes a node handle.
old-location: mscs\closeclusternode.htm
tech.root: mscs
ms.assetid: e2d90b7e-d181-48b6-a891-b885c24a15ea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CloseClusterNode, CloseClusterNode function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NODE, PCLUSAPI_CLOSE_CLUSTER_NODE function [Failover Cluster], _wolf_closeclusternode, clusapi/CloseClusterNode, clusapi/PCLUSAPI_CLOSE_CLUSTER_NODE, mscs.closeclusternode
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
 - CloseClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClusterNode function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to an existing node.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 

