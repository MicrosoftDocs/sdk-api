---
UID: NF:msinkaut.IInkDisp.DeleteStrokes
title: IInkDisp::DeleteStrokes (msinkaut.h)
description: Deletes an InkStrokes collection from the Strokes collection of the InkDisp object.
helpviewer_keywords: ["DeleteStrokes","DeleteStrokes method [Tablet PC]","DeleteStrokes method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","DeleteStrokes method","IInkDisp.DeleteStrokes","IInkDisp::DeleteStrokes","cbc11006-a434-46f8-a78c-3b67e35ed32a","msinkaut/IInkDisp::DeleteStrokes","tablet.inkdisp_deletestrokes"]
old-location: tablet\inkdisp_deletestrokes.htm
tech.root: tablet
ms.assetid: cbc11006-a434-46f8-a78c-3b67e35ed32a
ms.date: 12/05/2018
ms.keywords: DeleteStrokes, DeleteStrokes method [Tablet PC], DeleteStrokes method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],DeleteStrokes method, IInkDisp.DeleteStrokes, IInkDisp::DeleteStrokes, cbc11006-a434-46f8-a78c-3b67e35ed32a, msinkaut/IInkDisp::DeleteStrokes, tablet.inkdisp_deletestrokes
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
 - IInkDisp::DeleteStrokes
 - msinkaut/IInkDisp::DeleteStrokes
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
 - IInkDisp.DeleteStrokes
---

# IInkDisp::DeleteStrokes


## -description

Deletes an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection from the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a> collection of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -parameters

### -param Strokes [in, optional]

Optional. Specifies the collection of strokes to delete from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is <b>NULL</b>.

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
Cannot allocate memory that is used to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the strokes must match the known <b>InkDisp</b> object.

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

## -remarks

This method deletes all of the strokes in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object if no <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is passed in. To delete only one stroke at a time, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke</a> method.

The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object renumbers the indices of the remaining strokes in the <b>InkDisp</b> object if the strokes that were deleted do not fall at the end of the <b>InkDisp</b> object's collection of strokes.

<div class="alert"><b>Note</b>  The contents of a <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection become invalid when strokes that are contained in the collection are deleted from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.</div>
<div> </div>
<b>DeleteStrokes</b> can result in an error if called while the user is actively laying down ink.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
