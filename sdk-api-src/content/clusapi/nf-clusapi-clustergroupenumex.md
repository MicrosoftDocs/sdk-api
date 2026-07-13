---
UID: NF:clusapi.ClusterGroupEnumEx
title: ClusterGroupEnumEx function (clusapi.h)
description: Retrieves an item in the enumeration.
helpviewer_keywords: ["ClusterGroupEnumEx","ClusterGroupEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_ENUM_EX","PCLUSAPI_CLUSTER_GROUP_ENUM_EX function [Failover Cluster]","clusapi/ClusterGroupEnumEx","clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM_EX","mscs.clustergroupenumex"]
old-location: mscs\clustergroupenumex.htm
tech.root: MsCS
ms.assetid: 139FE5AB-9465-46F8-B360-F27F19D82A88
ms.date: 12/05/2018
ms.keywords: ClusterGroupEnumEx, ClusterGroupEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM_EX, mscs.clustergroupenumex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ClusterGroupEnumEx
 - clusapi/ClusterGroupEnumEx
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
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterGroupEnumEx
---

# ClusterGroupEnumEx function


## -description

Retrieves an item in the enumeration.The <b>PCLUSAPI_CLUSTER_GROUP_ENUM_EX</b> type defines a pointer to this function.

## -parameters

### -param hGroupEnumEx [in]

The handle to the enumeration from which the item will be retrieved.

### -param dwIndex [in]

The zero-based index of the item in the enumeration.

### -param pItem [in, out]

A pointer to the buffer to be filled.

### -param cbItem [in, out]

On input, the size of <i>pItem</i>.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.

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
<i>dwIndex</i> is larger than the number of items in the enumeration.

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

## -remarks

The <b>ClusterGroupEnumEx</b> function doesn't connect to the cluster, because the <i>hGroupEnumEx</i> already contains the enumeration data.  The data is copied into the buffer but no data is retrieved from the cluster.

