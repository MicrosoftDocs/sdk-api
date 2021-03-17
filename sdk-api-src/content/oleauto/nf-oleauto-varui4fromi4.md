---
UID: NF:oleauto.VarUI4FromI4
title: VarUI4FromI4 function (oleauto.h)
description: Converts a long value to an unsigned long value.
helpviewer_keywords: ["VarUI4FromI4","VarUI4FromI4 function [Automation]","_oa96_VarUI4FromI4","automat.varui4fromi4","oleauto/VarUI4FromI4"]
old-location: automat\varui4fromi4.htm
tech.root: automat
ms.assetid: 4a77c589-f7a2-475e-a087-f638f85ff00d
ms.date: 12/05/2018
ms.keywords: VarUI4FromI4, VarUI4FromI4 function [Automation], _oa96_VarUI4FromI4, automat.varui4fromi4, oleauto/VarUI4FromI4
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
 - VarUI4FromI4
 - oleauto/VarUI4FromI4
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
 - VarUI4FromI4
---

# VarUI4FromI4 function


## -description

Converts a long value to an unsigned long value.

## -parameters

### -param lIn [in]

The value to convert.

### -param pulOut [out]

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

