---
UID: NF:clusapi.GetClusterInformation
title: GetClusterInformation function
author: windows-sdk-content
description: Retrieves a cluster's name and version.
old-location: mscs\getclusterinformation.htm
tech.root: mscs
ms.assetid: 5b259eb9-c5d0-4f4f-8a6b-14eaed716612
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetClusterInformation, GetClusterInformation function [Failover Cluster], PCLUSAPI_GET_CLUSTER_INFORMATION, PCLUSAPI_GET_CLUSTER_INFORMATION function [Failover Cluster], _wolf_getclusterinformation, clusapi/GetClusterInformation, clusapi/PCLUSAPI_GET_CLUSTER_INFORMATION, mscs.getclusterinformation
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
 - GetClusterInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterInformation function


## -description


Retrieves a <a href="c_gly.htm">cluster's</a> name and version. The <b>PCLUSAPI_GET_CLUSTER_INFORMATION</b> type defines a pointer to this function.


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
      <a href="https://msdn.microsoft.com/e1cecdbc-f0e4-4ee8-9a97-14859ceba5fd">CLUSTERVERSIONINFO</a> structure describing the version 
      of the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>. When 
      <i>lpClusterInfo</i> is not <b>NULL</b>, the 
      <b>dwVersionInfoSize</b> member of this structure should be set as follows: 
      <code>lpClusterInfo-&gt;dwVersionInfoSize = sizeof(CLUSTERVERSIONINFO);</code>


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is one of the 
       possible values.




## -remarks



Note that <i>lpcchClusterName</i> refers to a count of characters and not a count of bytes, 
    and that the returned size does not include the terminating <b>NULL</b> in the count. For more 
    information on sizing buffers, see 
    <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/e1cecdbc-f0e4-4ee8-9a97-14859ceba5fd">CLUSTERVERSIONINFO</a>
 

 

