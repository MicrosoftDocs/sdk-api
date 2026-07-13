---
UID: NF:clusapi.ClusterRegQueryValue
title: ClusterRegQueryValue function (clusapi.h)
description: Returns the name, type, and data components associated with a value for an open cluster database key.
helpviewer_keywords: ["ClusterRegQueryValue","ClusterRegQueryValue function [Failover Cluster]","REG_BINARY","REG_DWORD","REG_DWORD_BIG_ENDIAN","REG_EXPAND_SZ","REG_MULTI_SZ","REG_NONE","REG_QWORD","REG_SZ","_wolf_clusterregqueryvalue","clusapi/ClusterRegQueryValue","mscs.clusterregqueryvalue"]
old-location: mscs\clusterregqueryvalue.htm
tech.root: MsCS
ms.assetid: 78ea27da-2b95-46df-b01e-4a3717276859
ms.date: 12/05/2018
ms.keywords: ClusterRegQueryValue, ClusterRegQueryValue function [Failover Cluster], REG_BINARY, REG_DWORD, REG_DWORD_BIG_ENDIAN, REG_EXPAND_SZ, REG_MULTI_SZ, REG_NONE, REG_QWORD, REG_SZ, _wolf_clusterregqueryvalue, clusapi/ClusterRegQueryValue, mscs.clusterregqueryvalue
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
 - ClusterRegQueryValue
 - clusapi/ClusterRegQueryValue
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
 - ClusterRegQueryValue
---

# ClusterRegQueryValue function


## -description

Returns the 
    name, type, and data components associated with a value for an open 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle of the cluster database key to query.

### -param lpszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to be queried.

### -param lpdwValueType [out, optional]

Pointer to the key's value type. This parameter can be <b>NULL</b> if the type is not 
       required; otherwise, the value returned through this parameter is one of the following.



#### REG_BINARY (3)

Binary data in any form.



#### REG_DWORD (4)

A 32-bit number.



#### REG_DWORD_BIG_ENDIAN (5)

A 32-bit number stored in big-endian format.



#### REG_EXPAND_SZ (2)

A null-terminated Unicode string that contains unexpanded references to environment variables (for example, 
         "%PATH%").



#### REG_MULTI_SZ (6)

A sequence of null-terminated strings, terminated by an empty string (\0).

The following is an example:

<i>String1</i>\0<i>String2</i>\0<i>String3</i>\0<i>LastString</i>\0\0

The first \0 terminates the first string, the second to the last \0 terminates the last string, and the 
         final \0 terminates the sequence. Note that the final terminator must be factored into the length of the 
         string.



#### REG_NONE (0)

No defined value type.



#### REG_QWORD (11)

A 64-bit number.



#### REG_SZ (1)

A null-terminated Unicode string.

### -param lpData [out, optional]

Pointer to the value's data. This parameter can be <b>NULL</b> if the data is not 
       required.

### -param lpcbData [in, out, optional]

On input, pointer to the count of bytes in the buffer pointed to by the <i>lpbData</i> 
       parameter. On output, pointer to the count of bytes in the value's data, which is placed in the content of 
       <i>lpbData</i> if the caller passes in a valid pointer.

The <i>lpbData</i> parameter can be <b>NULL</b> only if 
       <i>lpbData</i> is also <b>NULL</b>.

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
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

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
The buffer pointed to by <i>lpbData</i> is not large enough to hold the data for the 
         value. <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a> stores the 
         required size in the content of <i>lpbData</i>.

</td>
</tr>
</table>

## -remarks

If <i>lpbData</i> is <b>NULL</b>, the 
     <b>ClusterRegQueryValue</b> function returns <b>ERROR_SUCCESS</b> 
     and stores the size of the value's data in the content of <i>lpbData</i>. This information 
     allows the caller to correctly allocate a buffer to hold the data.

If <i>lpdwValueType</i> is set to <b>REG_SZ</b>, 
     <b>REG_MULTI_SZ</b> or <b>REG_EXPAND_SZ</b>, then 
     <i>lpbData</i> also includes a <b>NULL</b> terminator.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>