---
UID: NF:msinkaut.IInkDisp.DeleteStroke
title: IInkDisp::DeleteStroke (msinkaut.h)
description: Deletes a IInkStrokeDisp object from the InkDisp object.
helpviewer_keywords: ["DeleteStroke","DeleteStroke method [Tablet PC]","DeleteStroke method [Tablet PC]","IInkDisp interface","IInkDisp","IInkDisp interface [Tablet PC]","DeleteStroke method","IInkDisp.DeleteStroke","IInkDisp::DeleteStroke","ac6579ec-20f7-4a20-8cb8-5f3a6119959d","msinkaut/IInkDisp::DeleteStroke","tablet.inkdisp_deletestroke"]
old-location: tablet\inkdisp_deletestroke.htm
tech.root: tablet
ms.assetid: ac6579ec-20f7-4a20-8cb8-5f3a6119959d
ms.date: 12/05/2018
ms.keywords: DeleteStroke, DeleteStroke method [Tablet PC], DeleteStroke method [Tablet PC],IInkDisp interface, IInkDisp, IInkDisp interface [Tablet PC],DeleteStroke method, IInkDisp.DeleteStroke, IInkDisp::DeleteStroke, ac6579ec-20f7-4a20-8cb8-5f3a6119959d, msinkaut/IInkDisp::DeleteStroke, tablet.inkdisp_deletestroke
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
 - IInkDisp::DeleteStroke
 - msinkaut/IInkDisp::DeleteStroke
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
 - IInkDisp.DeleteStroke
---

# IInkDisp::DeleteStroke


## -description

Deletes a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -parameters

### -param Stroke [in]

 The stroke to delete from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

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

This method deletes only a single stroke. To delete a collection of strokes, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a> method.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
