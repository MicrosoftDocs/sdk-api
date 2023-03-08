---
UID: NF:msinkaut.IInkDisp.AddStrokesAtRectangle
title: IInkDisp::AddStrokesAtRectangle (msinkaut.h)
description: Adds a specified Strokes collection into this InkDisp object at a specified rectangle.
helpviewer_keywords: ["AddStrokesAtRectangle","AddStrokesAtRectangle method [Tablet PC]","AddStrokesAtRectangle method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","AddStrokesAtRectangle method","IInkDisp.AddStrokesAtRectangle","IInkDisp::AddStrokesAtRectangle","c5a7cbbc-361c-4e99-af31-f7114eb5261b","msinkaut/IInkDisp::AddStrokesAtRectangle","tablet.inkdisp_addstrokesatrectangle"]
old-location: tablet\inkdisp_addstrokesatrectangle.htm
tech.root: tablet
ms.assetid: c5a7cbbc-361c-4e99-af31-f7114eb5261b
ms.date: 12/05/2018
ms.keywords: AddStrokesAtRectangle, AddStrokesAtRectangle method [Tablet PC], AddStrokesAtRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],AddStrokesAtRectangle method, IInkDisp.AddStrokesAtRectangle, IInkDisp::AddStrokesAtRectangle, c5a7cbbc-361c-4e99-af31-f7114eb5261b, msinkaut/IInkDisp::AddStrokesAtRectangle, tablet.inkdisp_addstrokesatrectangle
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
 - IInkDisp::AddStrokesAtRectangle
 - msinkaut/IInkDisp::AddStrokesAtRectangle
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
 - IInkDisp.AddStrokesAtRectangle
---

# IInkDisp::AddStrokesAtRectangle


## -description

Adds a specified <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">Strokes</a> collection into this <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object at a specified rectangle.

## -parameters

### -param SourceStrokes [in]

 The strokes to add to the ink. These source strokes are appended to this <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

### -param TargetRectangle [in]

 The <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> in ink space coordinates where the strokes are added. A run-time error occurs if the coordinates of the rectangle are {0,0,0,0}.

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
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
A pointer does not point at a valid object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The rectangle's top and bottom are equal.

</td>
</tr>
</table>

## -remarks

When inserted, the strokes are scaled from the bounding box of the strokes to the rectangle.

This method can be used to copy strokes within a single <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The source ink strokes do not have to come from another <b>InkDisp</b> object.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
