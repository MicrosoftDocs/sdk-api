---
UID: NF:clusapi.GetClusterInformation
title: GetClusterInformation function (clusapi.h)
description: Retrieves a cluster's name and version.
helpviewer_keywords: ["GetClusterInformation","GetClusterInformation function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_INFORMATION","PCLUSAPI_GET_CLUSTER_INFORMATION function [Failover Cluster]","_wolf_getclusterinformation","clusapi/GetClusterInformation","clusapi/PCLUSAPI_GET_CLUSTER_INFORMATION","mscs.getclusterinformation"]
old-location: mscs\getclusterinformation.htm
tech.root: MsCS
ms.assetid: 5b259eb9-c5d0-4f4f-8a6b-14eaed716612
ms.date: 12/05/2018
ms.keywords: GetClusterInformation, GetClusterInformation function [Failover Cluster], PCLUSAPI_GET_CLUSTER_INFORMATION, PCLUSAPI_GET_CLUSTER_INFORMATION function [Failover Cluster], _wolf_getclusterinformation, clusapi/GetClusterInformation, clusapi/PCLUSAPI_GET_CLUSTER_INFORMATION, mscs.getclusterinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetClusterInformation
 - clusapi/GetClusterInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - GetClusterInformation
---

# GetClusterInformation function


## -description

Retrieves a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster's</a> name and version. The <b>PCLUSAPI_GET_CLUSTER_INFORMATION</b> type defines a pointer to this function.

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
      <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusterversioninfo">CLUSTERVERSIONINFO</a> structure describing the version 
      of the <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>. When 
      <i>lpClusterInfo</i> is not <b>NULL</b>, the 
      <b>dwVersionInfoSize</b> member of this structure should be set as follows: 
      <code>lpClusterInfo-&gt;dwVersionInfoSize = sizeof(CLUSTERVERSIONINFO);</code>

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is one of the 
       possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpszClusterName</i> is not big enough to hold the result. 
        The <i>lpcchClusterName</i> parameter returns the number of characters in the result, 
        excluding the terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchClusterName</i> refers to a count of characters and not a count of bytes, 
    and that the returned size does not include the terminating <b>NULL</b> in the count. For more 
    information on sizing buffers, see 
    <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusterversioninfo">CLUSTERVERSIONINFO</a>