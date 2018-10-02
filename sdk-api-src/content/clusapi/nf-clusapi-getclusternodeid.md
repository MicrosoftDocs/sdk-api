---
UID: NF:clusapi.GetClusterNodeId
title: GetClusterNodeId function
author: windows-sdk-content
description: Returns the unique identifier of a cluster node.
old-location: mscs\getclusternodeid.htm
tech.root: MsCS
ms.assetid: 976ca079-10f7-4e12-9033-07ea83e8c92a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetClusterNodeId, GetClusterNodeId function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NODE_ID, PCLUSAPI_GET_CLUSTER_NODE_ID function [Failover Cluster], _wolf_getclusternodeid, clusapi/GetClusterNodeId, clusapi/PCLUSAPI_GET_CLUSTER_NODE_ID, mscs.getclusternodeid
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - GetClusterNodeId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNodeId function


## -description


Returns the unique identifier of a cluster 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>. The <b>PCLUSAPI_GET_CLUSTER_NODE_ID</b> type defines a pointer to this function.


## -parameters




### -param hNode [in, optional]

Handle to the node with the identifier to be returned or <b>NULL</b>. If 
       <i>hNode</i> is set to <b>NULL</b>, the node identifier for the node on 
       which the application is running is returned in the content of <i>lpszNodeId</i>.


### -param lpszNodeId [out]

This parameter points to a buffer that receives the unique ID of <i>hNode</i>, including 
       the terminating <b>NULL</b> character.


### -param lpcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszNodeId</i> parameter, including the <b>NULL</b> terminator. On 
       output, pointer to the count of characters stored in the buffer excluding the <b>NULL</b> 
       terminator.


## -returns



This function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following are the 
       possible values:




## -remarks



The <b>PCLUSAPI_GET_CLUSTER_NODE_ID</b> type defines a pointer to this function.

If <i>hNode</i> is set to <b>NULL</b> and the caller is running on an 
     active cluster node, the <b>GetClusterNodeId</b> function 
     returns the identifier of the node on which the application is running. Setting <i>hNode</i> 
     to <b>NULL</b> is a convenient way for 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372239(v=VS.85).aspx">resource DLLs</a> to determine the node identifier of the node 
     they are running on. The <a href="https://msdn.microsoft.com/en-us/library/Bb394631(v=VS.85).aspx">GetCurrentClusterNodeId</a> 
     macro can be used instead of passing <b>NULL</b> for the <i>hNode</i> 
     parameter.

A cluster node identifier is a unique identifier that does not change even if the node's name is changed.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing 
     buffers, see <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb394631(v=VS.85).aspx">GetCurrentClusterNodeId</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 

