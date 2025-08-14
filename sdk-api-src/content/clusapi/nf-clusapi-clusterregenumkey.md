---
UID: NF:clusapi.ClusterRegEnumKey
title: ClusterRegEnumKey function (clusapi.h)
description: Enumerates the subkeys of an open cluster database key.
helpviewer_keywords: ["ClusterRegEnumKey","ClusterRegEnumKey function [Failover Cluster]","_wolf_clusterregenumkey","clusapi/ClusterRegEnumKey","mscs.clusterregenumkey"]
old-location: mscs\clusterregenumkey.htm
tech.root: MsCS
ms.assetid: ed70c16d-98d2-4d84-b5cd-1e5decc5b7bd
ms.date: 12/05/2018
ms.keywords: ClusterRegEnumKey, ClusterRegEnumKey function [Failover Cluster], _wolf_clusterregenumkey, clusapi/ClusterRegEnumKey, mscs.clusterregenumkey
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
 - ClusterRegEnumKey
 - clusapi/ClusterRegEnumKey
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegEnumKey
---

# ClusterRegEnumKey function


## -description

Enumerates the subkeys of an open 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

<b>HKEY</b> specifying a currently open key.

### -param dwIndex [in]

Index used to identify the next subkey to be enumerated. This parameter should be zero for the first call to 
       <b>ClusterRegEnumKey</b> and then incremented for 
       subsequent calls.

Because subkeys are not ordered, any new subkey has an arbitrary index. This means that 
       <b>ClusterRegEnumKey</b> may return subkeys in any 
       order.

### -param lpszName [out]

Pointer to a buffer that receives the name of the subkey, including the null-terminating character. The 
       function copies only the name of the subkey, not the full key hierarchy, to the buffer.

### -param lpcchName [in, out]

Pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

### -param lpftLastWriteTime [out, optional]

Pointer to the last time the enumerated subkey was modified.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
There are no more subkeys to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpszName</i> is not big enough to hold the result. The 
         <i>lpcchName</i> parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>

## -remarks

The <b>ClusterRegEnumKey</b> function retrieves 
     information about one subkey each time it is called.

Because <b>ClusterRegEnumKey</b> enumerates keys from 
     the root of the database on the node on which the application is running when <i>hKey</i> is 
     set to <b>NULL</b>, 
     <b>ClusterRegEnumKey</b> fails if the node is not part of 
     a cluster.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>