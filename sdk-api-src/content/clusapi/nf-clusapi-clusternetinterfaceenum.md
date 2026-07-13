---
UID: NF:clusapi.ClusterNetInterfaceEnum
title: ClusterNetInterfaceEnum function (clusapi.h)
description: Enumerates the network interfaces installed on a cluster, returning one name with each call.
helpviewer_keywords: ["ClusterNetInterfaceEnum","ClusterNetInterfaceEnum function [Failover Cluster]","clusapi/ClusterNetInterfaceEnum","mscs.clusternetinterfaceenum"]
old-location: mscs\clusternetinterfaceenum.htm
tech.root: MsCS
ms.assetid: 691362e9-88ba-4f10-8fde-eebcc72157b4
ms.date: 12/05/2018
ms.keywords: ClusterNetInterfaceEnum, ClusterNetInterfaceEnum function [Failover Cluster], clusapi/ClusterNetInterfaceEnum, mscs.clusternetinterfaceenum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterNetInterfaceEnum
 - clusapi/ClusterNetInterfaceEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ClusAPI.dll
api_name:
 - ClusterNetInterfaceEnum
---

# ClusterNetInterfaceEnum function


## -description

Enumerates the <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a> installed on a 
    cluster, returning one name with each call.

## -parameters

### -param hNetInterfaceEnum [in]

Handle to an existing enumeration object originally returned by the 
       <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusternetinterfaceopenenum">ClusterNetInterfaceOpenEnum</a> function.

### -param dwIndex [in]

Index used to identify the entry to be enumerated. This parameter should be zero for the first call and then incremented for each subsequent 
       call.

### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the returned object.

### -param lpcchName [in, out]

Pointer to the size, in characters, of the <i>lpszName</i> buffer. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, indicates the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

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
The operation completed successfully.

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
No more data is available. This value is returned if there are no more objects to be 
         returned.

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
More data is available. This value is returned if the buffer pointed to by 
         <i>lpszName</i> is not big enough to hold the result. The 
         <i>lpcchName</i> parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

</td>
</tr>
</table>