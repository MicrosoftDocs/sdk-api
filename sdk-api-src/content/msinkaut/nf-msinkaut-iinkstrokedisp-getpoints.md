---
UID: NF:msinkaut.IInkStrokeDisp.GetPoints
title: IInkStrokeDisp::GetPoints (msinkaut.h)
description: Retrieves the points that make up a stroke.
helpviewer_keywords: ["76378521-15d1-48a0-ae9f-8362faf60c9f","GetPoints","GetPoints method [Tablet PC]","GetPoints method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","GetPoints method","IInkStrokeDisp.GetPoints","IInkStrokeDisp::GetPoints","msinkaut/IInkStrokeDisp::GetPoints","tablet.iinkstrokedisp_getpoints"]
old-location: tablet\iinkstrokedisp_getpoints.htm
tech.root: tablet
ms.assetid: 76378521-15d1-48a0-ae9f-8362faf60c9f
ms.date: 12/05/2018
ms.keywords: 76378521-15d1-48a0-ae9f-8362faf60c9f, GetPoints, GetPoints method [Tablet PC], GetPoints method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPoints method, IInkStrokeDisp.GetPoints, IInkStrokeDisp::GetPoints, msinkaut/IInkStrokeDisp::GetPoints, tablet.iinkstrokedisp_getpoints
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokeDisp::GetPoints
 - msinkaut/IInkStrokeDisp::GetPoints
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokeDisp.GetPoints
---

# IInkStrokeDisp::GetPoints


## -description

Retrieves the points that make up a stroke.

## -parameters

### -param Index [in, optional]

Optional. The starting index within the array of points that make up the stroke. The default value ISC_FirstElement, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies the first point.

### -param Count [in, optional]

Optional. The number of points to return. The default value ISC_AllElements, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.

### -param Points [out, retval]

When this method returns, contains the array of points from the stroke.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory for the points.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index (out of range).

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
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ItemSelectionConstants Enumeration</a>