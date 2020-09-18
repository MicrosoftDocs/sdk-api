---
UID: NF:msinkaut15.IInkDivisionResult.ResultByType
title: IInkDivisionResult::ResultByType (msinkaut15.h)
description: Gets the requested structural units of the analysis results for an IInkDivisionUnits collection.
helpviewer_keywords: ["IInkDivisionResult interface [Tablet PC]","ResultByType method","IInkDivisionResult.ResultByType","IInkDivisionResult::ResultByType","ResultByType","ResultByType method [Tablet PC]","ResultByType method [Tablet PC]","IInkDivisionResult interface","d0bad0e8-e48c-443b-b52e-e95de3158710","msinkaut15/IInkDivisionResult::ResultByType","tablet.iinkdivisionresult_resultbytype"]
old-location: tablet\iinkdivisionresult_resultbytype.htm
tech.root: tablet
ms.assetid: d0bad0e8-e48c-443b-b52e-e95de3158710
ms.date: 12/05/2018
ms.keywords: IInkDivisionResult interface [Tablet PC],ResultByType method, IInkDivisionResult.ResultByType, IInkDivisionResult::ResultByType, ResultByType, ResultByType method [Tablet PC], ResultByType method [Tablet PC],IInkDivisionResult interface, d0bad0e8-e48c-443b-b52e-e95de3158710, msinkaut15/IInkDivisionResult::ResultByType, tablet.iinkdivisionresult_resultbytype
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivisionResult::ResultByType
 - msinkaut15/IInkDivisionResult::ResultByType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionResult.ResultByType
---

# IInkDivisionResult::ResultByType


## -description

Gets the requested structural units of the analysis results for an <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection.

## -parameters

### -param divisionType [in]

The <a href="/windows/desktop/api/msinkaut15/ne-msinkaut15-inkdivisiontype">InkDivisionType</a> enumeration value that indicates the structural units to return.

### -param InkDivisionUnits [out, retval]

A pointer to the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection that contains the requested structural units of the analysis results.

## -returns

This method can return one of these values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -remarks

This method returns a new <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection each time the method is called.

If no structural units of the requested type exist in the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object, then this method returns an empty <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult Interface</a>



<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>



<a href="/windows/desktop/api/msinkaut15/ne-msinkaut15-inkdivisiontype">InkDivisionType Enumeration</a>