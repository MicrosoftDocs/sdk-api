---
UID: NC:clusapi.PCLUSAPI_ADD_CLUSTER_NODE
title: PCLUSAPI_ADD_CLUSTER_NODE
author: windows-sdk-content
description: Adds a node to an existing cluster.
old-location: mscs\addclusternode.htm
old-project: MsCS
ms.assetid: e1d3611e-10d1-4858-923a-01633d2ed78b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_ADD_CLUSTER_NODE, PCLUSAPI_ADD_CLUSTER_NODE callback, PCLUSAPI_ADD_CLUSTER_NODE callback function [Failover Cluster], clusapi/PCLUSAPI_ADD_CLUSTER_NODE, mscs.addclusternode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - PCLUSAPI_ADD_CLUSTER_NODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ADD_CLUSTER_NODE callback function


## -description


Adds a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to an existing cluster. The <b>PCLUSAPI_ADD_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster, returned by the <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a> or 
       <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function.


### -param lpszNodeName [in]

Name of the computer to add to the cluster.


### -param pfnProgressCallback [in, optional]

Optional address to a 
       <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
       callback function.


### -param pvCallbackArg [in, optional]

Argument for the callback function.


## -returns



Handle to the new node or <b>NULL</b> to indicate that the node was not successfully added 
       to the cluster. For more information about the error, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



After the <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function successfully 
     completes, at least 30 seconds should be allowed before the 
     <i>AddClusterNode</i> function is called to add additional 
     nodes.




## -see-also




<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>



<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

