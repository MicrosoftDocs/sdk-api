---
UID: NF:oleauto.VarUI1FromStr
title: VarUI1FromStr function (oleauto.h)
description: Converts an OLECHAR string to an unsigned char string.
helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VarUI1FromStr","VarUI1FromStr function [Automation]","_oa96_VarUI1FromStr","automat.varui1fromstr","oleauto/VarUI1FromStr"]
old-location: automat\varui1fromstr.htm
tech.root: automat
ms.assetid: cd21a474-d75f-40ad-aa5a-43eda74e6b2b
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VarUI1FromStr, VarUI1FromStr function [Automation], _oa96_VarUI1FromStr, automat.varui1fromstr, oleauto/VarUI1FromStr
f1_keywords:
- oleauto/VarUI1FromStr
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarUI1FromStr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarUI1FromStr function


## -description


Converts an OLECHAR string to an unsigned char string.


## -parameters




### -param strIn [in]

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
</table>
 


### -param pbOut [out]

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
 



