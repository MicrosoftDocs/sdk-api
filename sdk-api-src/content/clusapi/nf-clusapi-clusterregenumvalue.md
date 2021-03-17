---
UID: NF:clusapi.ClusterRegEnumValue
title: ClusterRegEnumValue function (clusapi.h)
description: Enumerates the values of an open cluster database key.
helpviewer_keywords: ["ClusterRegEnumValue","ClusterRegEnumValue function [Failover Cluster]","REG_BINARY","REG_DWORD","REG_DWORD_BIG_ENDIAN","REG_EXPAND_SZ","REG_MULTI_SZ","REG_NONE","REG_QWORD","REG_SZ","_wolf_clusterregenumvalue","clusapi/ClusterRegEnumValue","mscs.clusterregenumvalue"]
old-location: mscs\clusterregenumvalue.htm
tech.root: MsCS
ms.assetid: 4ea2fc6f-6b52-4fa1-8d71-5bbae72368b3
ms.date: 12/05/2018
ms.keywords: ClusterRegEnumValue, ClusterRegEnumValue function [Failover Cluster], REG_BINARY, REG_DWORD, REG_DWORD_BIG_ENDIAN, REG_EXPAND_SZ, REG_MULTI_SZ, REG_NONE, REG_QWORD, REG_SZ, _wolf_clusterregenumvalue, clusapi/ClusterRegEnumValue, mscs.clusterregenumvalue
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
 - ClusterRegEnumValue
 - clusapi/ClusterRegEnumValue
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
 - ClusterRegEnumValue
---

# ClusterRegEnumValue function


## -description

Enumerates the 
    values of an open <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle of the cluster database key to enumerate.

### -param dwIndex [in]

Index used to identify the next value to be enumerated. This parameter should be zero for the first call to 
       <b>ClusterRegEnumValue</b> and then incremented for 
       subsequent calls.

Because values are not ordered, any new value has an arbitrary index. This means that 
       <b>ClusterRegEnumValue</b> may return values in any 
       order.

### -param lpszValueName [out]

Pointer to a null-terminated Unicode string containing the name of the returned value.

### -param lpcchValueName [in, out]

Pointer to the size of the <i>lpszValueName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

### -param lpdwType [out, optional]

Pointer to the type code for the value entry, or <b>NULL</b> if the type code is not 
       required. The type code can be one of the following values.



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

Pointer to the data for the value entry. This parameter can be <b>NULL</b> if the data is 
       not required.

### -param lpcbData [in, out, optional]

On input, pointer to a count of bytes in the buffer pointed to by the <i>lpbData</i> 
       parameter. On output, pointer to a count of bytes resulting from the operation. This parameter can be 
       <b>NULL</b> only if <i>lpbData</i> is <b>NULL</b>.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
There are no more values to be returned.

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
One of the output buffers (<i>lpszValueName</i> or <i>lpbData</i>) is 
         too small to hold the resulting data. The <i>lpcchValueName</i> and the 
         <i>lpbData</i> parameters indicate the required size (note that 
         <i>lpcchValueName</i> does not include the terminating <b>NULL</b> in 
         the character count).

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

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>