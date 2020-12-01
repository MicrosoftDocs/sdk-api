---
UID: NF:msinkaut.IInkStrokeDisp.SetPoints
title: IInkStrokeDisp::SetPoints (msinkaut.h)
description: Sets the points of the IInkStrokeDisp using an array of X, Y values.
helpviewer_keywords: ["759e3195-e1de-45eb-a9de-8ec8fe2347c1","IInkStrokeDisp interface [Tablet PC]","SetPoints method","IInkStrokeDisp.SetPoints","IInkStrokeDisp::SetPoints","SetPoints","SetPoints method [Tablet PC]","SetPoints method [Tablet PC]","IInkStrokeDisp interface","msinkaut/IInkStrokeDisp::SetPoints","tablet.iinkstrokedisp_setpoints"]
old-location: tablet\iinkstrokedisp_setpoints.htm
tech.root: tablet
ms.assetid: 759e3195-e1de-45eb-a9de-8ec8fe2347c1
ms.date: 12/05/2018
ms.keywords: 759e3195-e1de-45eb-a9de-8ec8fe2347c1, IInkStrokeDisp interface [Tablet PC],SetPoints method, IInkStrokeDisp.SetPoints, IInkStrokeDisp::SetPoints, SetPoints, SetPoints method [Tablet PC], SetPoints method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::SetPoints, tablet.iinkstrokedisp_setpoints
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
 - IInkStrokeDisp::SetPoints
 - msinkaut/IInkStrokeDisp::SetPoints
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
 - IInkStrokeDisp.SetPoints
---

# IInkStrokeDisp::SetPoints


## -description

Sets the points of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> using an array of X, Y values.

## -parameters

### -param Points [in]

The array of new points to replace the points in the stroke beginning at <i>index</i>. This is a VARIANT containing an array of Long with the points represented by alternating values of the form x0, y0, x1, y1, x2, y2, and so on.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Index [in, optional]

Optional. The zero-based index of the first point in the stroke to be modified. The default value <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ISC_FirstElement</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies that the first point in the stroke is modified.

### -param Count [in, optional]

Optional. The count of points in the stroke to be modified. The default value <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ISC_AllElements</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies that all points in the stroke are modified.

### -param NumberOfPointsSet [out, retval]

When this method returns, contains the actual number of packets set.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>index</i> (out of range), or <i>points</i> parameter. Was not in the correct format.

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

This method does not change the number of points in the stroke. To change the number of points in the stroke, a new stroke must be created, or the stroke must be split.

This method does not provide for truncating the stroke. If the points array contains fewer points than the stroke, the remainder of the points in the stroke are not be modified.

This method does not provide for extending the stroke. If the points array contains more points than the stroke, the extra points are not used. If the count exceeds the number of points in the array, only the number of points in the array are modified.

In order to draw the stroke after calling <b>SetPoints</b>, call the <a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a> function.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ItemSelectionConstants Enumeration</a>