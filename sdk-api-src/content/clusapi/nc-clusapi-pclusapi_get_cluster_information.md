---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_INFORMATION
title: PCLUSAPI_GET_CLUSTER_INFORMATION
author: windows-sdk-content
description: Retrieves a cluster's name and version.
old-location: mscs\getclusterinformation.htm
old-project: mscs
ms.assetid: 5b259eb9-c5d0-4f4f-8a6b-14eaed716612
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_INFORMATION, PCLUSAPI_GET_CLUSTER_INFORMATION callback, PCLUSAPI_GET_CLUSTER_INFORMATION callback function [Failover Cluster], _wolf_getclusterinformation, clusapi/PCLUSAPI_GET_CLUSTER_INFORMATION, mscs.getclusterinformation
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
 - PCLUSAPI_GET_CLUSTER_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_INFORMATION callback function


## -description


Retrieves a <a href="https://msdn.microsoft.com/library/ms682005(v=VS.85).aspx">cluster's</a> name and version. The <b>PCLUSAPI_GET_CLUSTER_INFORMATION</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster.


### -param lpszClusterName [out]

Pointer to a null-terminated Unicode string containing the name of the cluster identified by 
      <i>hCluster</i>.


### -param lpcchClusterName [in, out]

Pointer to the size of the <i>lpszClusterName</i> buffer as a count of characters. On 
      input, specify the maximum number of characters the buffer can hold, including the terminating 
      <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
      the terminating <b>NULL</b>.


### -param lpClusterInfo [out, optional]

Either <b>NULL</b> or a pointer to a 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369056(v=VS.85).aspx">CLUSTERVERSIONINFO</a> structure describing the version 
      of the <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a>. When 
      <i>lpClusterInfo</i> is not <b>NULL</b>, the 
      <b>dwVersionInfoSize</b> member of this structure should be set as follows: 
      <code>lpClusterInfo-&gt;dwVersionInfoSize = sizeof(CLUSTERVERSIONINFO);</code>


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following is one of the 
       possible values.




## -remarks



Note that <i>lpcchClusterName</i> refers to a count of characters and not a count of bytes, 
    and that the returned size does not include the terminating <b>NULL</b> in the count. For more 
    information on sizing buffers, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369056(v=VS.85).aspx">CLUSTERVERSIONINFO</a>
 

 

