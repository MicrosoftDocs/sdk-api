---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER
title: PCLUSAPI_CLOSE_CLUSTER
author: windows-sdk-content
description: Closes a cluster handle.
old-location: mscs\closecluster.htm
old-project: MsCS
ms.assetid: cf055fd6-b1e1-4262-b205-c7d926522450
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER, PCLUSAPI_CLOSE_CLUSTER callback, PCLUSAPI_CLOSE_CLUSTER callback function [Failover Cluster], _wolf_closecluster, clusapi/PCLUSAPI_CLOSE_CLUSTER, mscs.closecluster
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
 - PCLUSAPI_CLOSE_CLUSTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER callback function


## -description


Closes a cluster handle. The <b>PCLUSAPI_CLOSE_CLUSTER</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster to close.


## -returns



This function always returns <b>TRUE</b>.




## -remarks



Do not close a cluster handle if there are any object handles still in use that were obtained from the cluster 
    handle. After a cluster handle has been closed, all handles obtained from that handle are invalid.


#### Examples

See <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

