---
UID: NF:clusapi.GetNodeClusterState
title: GetNodeClusterState function
author: windows-sdk-content
description: Determines whether the Cluster service is installed and running on a node.
old-location: mscs\getnodeclusterstate.htm
tech.root: mscs
ms.assetid: 67534bc8-f19e-4330-850a-788a7f031f5b
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ClusterStateNotConfigured, ClusterStateNotInstalled, ClusterStateNotRunning, ClusterStateRunning, GetNodeClusterState, GetNodeClusterState function [Failover Cluster], PCLUSAPI_GET_NODE_CLUSTER_STATE, PCLUSAPI_GET_NODE_CLUSTER_STATE function [Failover Cluster], _wolf_getnodeclusterstate, clusapi/GetNodeClusterState, clusapi/PCLUSAPI_GET_NODE_CLUSTER_STATE, mscs.getnodeclusterstate
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
 - GetNodeClusterState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNodeClusterState function


## -description


Determines whether the <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> is installed and 
    running on a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>. The <b>PCLUSAPI_GET_NODE_CLUSTER_STATE</b> type defines a pointer to this function.


## -parameters




### -param lpszNodeName [in, optional]

Pointer to a null-terminated Unicode string containing the name of the node to query. If 
       <i>lpszNodeName</i> is <b>NULL</b>, the local node is queried.


### -param pdwClusterState [out]

Pointer to a value describing the state of the Cluster service on the node. A node will be described by one 
       of the following <a href="https://msdn.microsoft.com/en-us/library/Bb394679(v=VS.85).aspx">NODE_CLUSTER_STATE</a> enumeration 
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
       fails, the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



<b>Note</b>  The <b>GetNodeClusterState</b> function does not 
     support a 64-bit Windows-based <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> if the calling application is 
     32-bit Windows-based.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb394679(v=VS.85).aspx">NODE_CLUSTER_STATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>
 

 

