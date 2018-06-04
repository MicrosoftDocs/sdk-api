---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PCLUSAPI_GET_NODE_CLUSTER_STATE callback function


## -description


Determines whether the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> is installed and 
    running on a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>. The <b>PCLUSAPI_GET_NODE_CLUSTER_STATE</b> type defines a pointer to this function.


## -parameters




### -param lpszNodeName [in, optional]

Pointer to a null-terminated Unicode string containing the name of the node to query. If 
       <i>lpszNodeName</i> is <b>NULL</b>, the local node is queried.


### -param pdwClusterState [out]

Pointer to a value describing the state of the Cluster service on the node. A node will be described by one 
       of the following <a href="https://msdn.microsoft.com/cc3b5bdc-79d7-4578-bfa5-8e57df4670e6">NODE_CLUSTER_STATE</a> enumeration 
       values.



#### ClusterStateNotInstalled (0)

The Cluster service is not installed on the node.



#### ClusterStateNotConfigured (1)

The Cluster service is installed on the node but has not yet been configured.



#### ClusterStateNotRunning (3)

The Cluster service is installed and configured on the node but is not currently running.



#### ClusterStateRunning (19 (0x13))

The Cluster service is installed, configured, and running on the node.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0). If the operation 
       fails, the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>Note</b>  The <i>GetNodeClusterState</i> function does not 
     support a 64-bit Windows-based <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> if the calling application is 
     32-bit Windows-based.




## -see-also




<a href="https://msdn.microsoft.com/cc3b5bdc-79d7-4578-bfa5-8e57df4670e6">NODE_CLUSTER_STATE</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

