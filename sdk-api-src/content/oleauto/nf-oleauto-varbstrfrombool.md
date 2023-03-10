---
UID: NF:oleauto.VarBstrFromBool
title: VarBstrFromBool function (oleauto.h)
description: Converts a Boolean value to a BSTR value.
helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VAR_LOCALBOOL","VarBstrFromBool","VarBstrFromBool function [Automation]","_oa96_VarBstrFromBool","automat.varbstrfrombool","oleauto/VarBstrFromBool"]
old-location: automat\varbstrfrombool.htm
tech.root: automat
ms.assetid: 6dc363bc-366c-4d9f-8aed-b1aed752c04f
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VAR_LOCALBOOL, VarBstrFromBool, VarBstrFromBool function [Automation], _oa96_VarBstrFromBool, automat.varbstrfrombool, oleauto/VarBstrFromBool
req.header: oleauto.h
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
 - VarBstrFromBool
 - oleauto/VarBstrFromBool
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
 - VarBstrFromBool
---

# VarBstrFromBool function


## -description

Converts a Boolean value to a BSTR value.

## -parameters

### -param boolIn [in]

The value to convert.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

One or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOCALE_NOUSEROVERRIDE"></a><a id="locale_nouseroverride"></a><dl>
<dt><b>LOCALE_NOUSEROVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Uses the system default locale settings, rather than custom locale settings.

</td>
</tr>
<tr>
<td width="40%"><a id="VAR_LOCALBOOL"></a><a id="var_localbool"></a><dl>
<dt><b>VAR_LOCALBOOL</b></dt>
</dl>
</td>
<td width="60%">
Uses localized Boolean names.

</td>
</tr>
</table>

### -param pbstrOut [out]

The resulting value.

## -returns

This function can return one of these values.

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
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by the output parameter does not fit in the destination type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

