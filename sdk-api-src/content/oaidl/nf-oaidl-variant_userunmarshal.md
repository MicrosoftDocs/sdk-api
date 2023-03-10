---
UID: NF:oaidl.VARIANT_UserUnmarshal
title: VARIANT_UserUnmarshal function (oaidl.h)
description: Unmarshals a VARIANT object from the RPC buffer. (VARIANT_UserUnmarshal)
helpviewer_keywords: ["VARIANT_UserUnmarshal","VARIANT_UserUnmarshal function [Automation]","_oa96_VARIANT_UserUnmarshal","automat.variant_userunmarshal","oaidl/VARIANT_UserUnmarshal"]
old-location: automat\variant_userunmarshal.htm
tech.root: automat
ms.assetid: ec7de7f3-f64a-4ec5-9b92-450bb7d6b37b
ms.date: 12/05/2018
ms.keywords: VARIANT_UserUnmarshal, VARIANT_UserUnmarshal function [Automation], _oa96_VARIANT_UserUnmarshal, automat.variant_userunmarshal, oaidl/VARIANT_UserUnmarshal
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - VARIANT_UserUnmarshal
 - oaidl/VARIANT_UserUnmarshal
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
 - VARIANT_UserUnmarshal
---

# VARIANT_UserUnmarshal function


## -description

Unmarshals a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> object from the RPC buffer.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer. This pointer may or may not be aligned on entry.

### -param unnamedParam3 [out]

The object.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not valid.

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
The stub data for the buffer size is incorrect.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE
</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for this function to perform.

</td>
</tr>
</table>
