---
UID: NF:oleauto.VarI2FromDisp
title: VarI2FromDisp function (oleauto.h)
description: Converts the default property of an IDispatch instance to a short value.
helpviewer_keywords: ["VarI2FromDisp","VarI2FromDisp function [Automation]","_oa96_VarI2FromDisp","automat.vari2fromdisp","oleauto/VarI2FromDisp"]
old-location: automat\vari2fromdisp.htm
tech.root: automat
ms.assetid: 37c3084d-828a-42b4-92c3-d4c89336cac7
ms.date: 12/05/2018
ms.keywords: VarI2FromDisp, VarI2FromDisp function [Automation], _oa96_VarI2FromDisp, automat.vari2fromdisp, oleauto/VarI2FromDisp
f1_keywords:
- oleauto/VarI2FromDisp
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
- VarI2FromDisp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarI2FromDisp function


## -description


Converts the default property of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> instance to a short value.


## -parameters




### -param pdispIn

The value to convert.


### -param lcid [in]

The locale identifier.


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
 



