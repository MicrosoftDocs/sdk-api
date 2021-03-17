---
UID: NF:clusapi.ClusterEnumEx
title: ClusterEnumEx function (clusapi.h)
description: Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.
helpviewer_keywords: ["ClusterEnumEx","ClusterEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_ENUM_EX","PCLUSAPI_CLUSTER_ENUM_EX function [Failover Cluster]","clusapi/ClusterEnumEx","clusapi/PCLUSAPI_CLUSTER_ENUM_EX","mscs.clusterenumex"]
old-location: mscs\clusterenumex.htm
tech.root: MsCS
ms.assetid: F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5
ms.date: 12/05/2018
ms.keywords: ClusterEnumEx, ClusterEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_ENUM_EX, PCLUSAPI_CLUSTER_ENUM_EX function [Failover Cluster], clusapi/ClusterEnumEx, clusapi/PCLUSAPI_CLUSTER_ENUM_EX, mscs.clusterenumex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterEnumEx
 - clusapi/ClusterEnumEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterEnumEx
---

# ClusterEnumEx function


## -description

Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.

## -parameters

### -param hClusterEnum [in]

A handle to the enumerator that is returned by the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a> function.

### -param dwIndex [in]

The index that identifies the next cluster object to enumerate. This parameter should be zero for the first call to the  <b>ClusterEnumEx</b>  function and then be  incremented for subsequent calls.

### -param pItem [in, out]

A pointer that receives the returned cluster object properties.

### -param cbItem [in, out]

On input, the size of the  <i>pItem</i>   parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes that are  written into the buffer.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i>  parameter is larger than the number of items in the enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The buffer was filled successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_enum_item">CLUSTER_ENUM_ITEM</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>