---
UID: NF:oleauto.VarI2FromDate
title: VarI2FromDate function (oleauto.h)
description: Converts a date value to a short value.helpviewer_keywords: ["VarI2FromDate","VarI2FromDate function [Automation]","_oa96_VarI2FromDate","automat.vari2fromdate","oleauto/VarI2FromDate"]
old-location: automat\vari2fromdate.htm
tech.root: automat
ms.assetid: e4b86c29-5fc5-45dd-9ed1-7aa2bf8946dc
ms.date: 12/05/2018
ms.keywords: VarI2FromDate, VarI2FromDate function [Automation], _oa96_VarI2FromDate, automat.vari2fromdate, oleauto/VarI2FromDate
f1_keywords:
- oleauto/VarI2FromDate
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
- VarI2FromDate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarI2FromDate function


## -description


Converts a date value to a short value.


## -parameters




### -param dateIn [in]

The value to convert.


### -param psOut [out]

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
 



