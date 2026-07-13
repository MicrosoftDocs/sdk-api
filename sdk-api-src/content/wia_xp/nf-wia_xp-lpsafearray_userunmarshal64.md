---
UID: NF:wia_xp.LPSAFEARRAY_UserUnmarshal64
title: LPSAFEARRAY_UserUnmarshal64 function (wia_xp.h)
description: Unmarshals a SAFEARRAY object from the RPC buffer. (LPSAFEARRAY_UserUnmarshal64)
helpviewer_keywords: ["LPSAFEARRAY_UserUnmarshal64","LPSAFEARRAY_UserUnmarshal64 function [Automation]","automat.lpsafearray_userunmarshal64","wia_xp/LPSAFEARRAY_UserUnmarshal64"]
old-location: automat\lpsafearray_userunmarshal64.htm
tech.root: wia
ms.assetid: 19B52C54-0905-446C-A8D9-C98153931708
ms.date: 12/05/2018
ms.keywords: LPSAFEARRAY_UserUnmarshal64, LPSAFEARRAY_UserUnmarshal64 function [Automation], automat.lpsafearray_userunmarshal64, wia_xp/LPSAFEARRAY_UserUnmarshal64
req.header: wia_xp.h
req.include-header: Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPSAFEARRAY_UserUnmarshal64
 - wia_xp/LPSAFEARRAY_UserUnmarshal64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LPSAFEARRAY_UserUnmarshal64
archived: true
---

# LPSAFEARRAY_UserUnmarshal64 function


## -description

Unmarshals a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> object from the RPC buffer.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in, out]

The current buffer. This pointer may or may not be aligned on entry. The function aligns the buffer pointer, marshals the data, and returns the new buffer position, which is the address of the first byte after the marshaled object.

### -param unnamedParam3 [in]

Receives the safe array that contains the data.

## -returns

The value obtained from the returned <b>HRESULT</b> value is one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_BAD_STUB_DATA
</b></dt>
</dl>
</td>
<td width="60%">
The stub has received bad data.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED
</b></dt>
</dl>
</td>
<td width="60%">
The array could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for this function to perform.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADCALLEE
</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> object does not have the correct dimensions, does not have the correct features, or memory cannot be reallocated.

</td>
</tr>
</table>
