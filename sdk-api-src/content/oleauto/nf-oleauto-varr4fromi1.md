---
UID: NF:oleauto.VarR4FromI1
title: VarR4FromI1 function (oleauto.h)
description: Onverts a char value to a float value.helpviewer_keywords: ["VarR4FromI1","VarR4FromI1 function [Automation]","_oa96_VarR4FromI1","automat.varr4fromi1","oleauto/VarR4FromI1"]
old-location: automat\varr4fromi1.htm
tech.root: automat
ms.assetid: a8996080-98a7-439d-a300-3fd3930872fb
ms.date: 12/05/2018
ms.keywords: VarR4FromI1, VarR4FromI1 function [Automation], _oa96_VarR4FromI1, automat.varr4fromi1, oleauto/VarR4FromI1
f1_keywords:
- oleauto/VarR4FromI1
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
- VarR4FromI1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarR4FromI1 function


## -description


Converts a char value to a float value.


## -parameters




### -param cIn [in]

The value to convert.


### -param pfltOut [out]

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
 



