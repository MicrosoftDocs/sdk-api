---
UID: NF:oleauto.VarBstrCmp
title: VarBstrCmp function (oleauto.h)
description: Compares two variants of type BSTR.
helpviewer_keywords: ["NORM_IGNORECASE","NORM_IGNOREKANATYPE","NORM_IGNOREKASHIDA","NORM_IGNORENONSPACE","NORM_IGNORESYMBOLS","NORM_IGNOREWIDTH","VarBstrCmp","VarBstrCmp function [Automation]","_oa96_VarBstrCmp","automat.varbstrcmp","oleauto/VarBstrCmp"]
old-location: automat\varbstrcmp.htm
tech.root: automat
ms.assetid: 0b7d8735-19d5-4f6e-8b55-05f2c73ef3f8
ms.date: 12/05/2018
ms.keywords: NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNOREKASHIDA, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, VarBstrCmp, VarBstrCmp function [Automation], _oa96_VarBstrCmp, automat.varbstrcmp, oleauto/VarBstrCmp
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
 - VarBstrCmp
 - oleauto/VarBstrCmp
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
 - VarBstrCmp
---

# VarBstrCmp function


## -description

Compares two variants of type BSTR.

## -parameters

### -param bstrLeft [in]

The first variant.

### -param bstrRight [in]

The second variant.

### -param lcid [in]

The locale identifier of the program to determine whether UNICODE or ANSI strings are being used.

### -param dwFlags [in]

The following are compare results flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORECASE"></a><a id="norm_ignorecase"></a><dl>
<dt><b>NORM_IGNORECASE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Ignore case.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Ignore nonspace characters.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORESYMBOLS"></a><a id="norm_ignoresymbols"></a><dl>
<dt><b>NORM_IGNORESYMBOLS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Ignore symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREWIDTH"></a><a id="norm_ignorewidth"></a><dl>
<dt><b>NORM_IGNOREWIDTH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Ignore string width.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKANATYPE"></a><a id="norm_ignorekanatype"></a><dl>
<dt><b>NORM_IGNOREKANATYPE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Ignore Kana type.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKASHIDA"></a><a id="norm_ignorekashida"></a><dl>
<dt><b>NORM_IGNOREKASHIDA</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Ignore Arabic kashida characters.

</td>
</tr>
</table>

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_LT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>bstrLeft</i> is less than <i>bstrRight</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_EQ</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The parameters are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VARCMP_GT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>bstrLeft</i> is greater than <i>bstrRight</i>.

</td>
</tr>
</table>

## -remarks

This function will not compare arrays or records.

