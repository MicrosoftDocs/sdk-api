---
UID: NF:msinkaut.IInkStrokeDisp.ScaleToRectangle
title: IInkStrokeDisp::ScaleToRectangle (msinkaut.h)
description: Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object.helpviewer_keywords: ["8bc22004-3781-4018-9a92-88958039248c","IInkStrokeDisp interface [Tablet PC]","ScaleToRectangle method","IInkStrokeDisp.ScaleToRectangle","IInkStrokeDisp::ScaleToRectangle","ScaleToRectangle","ScaleToRectangle method [Tablet PC]","ScaleToRectangle method [Tablet PC]","IInkStrokeDisp interface","msinkaut/IInkStrokeDisp::ScaleToRectangle","tablet.iinkstrokedisp_scaletorectangle"]
old-location: tablet\iinkstrokedisp_scaletorectangle.htm
tech.root: tablet
ms.assetid: 8bc22004-3781-4018-9a92-88958039248c
ms.date: 12/05/2018
ms.keywords: 8bc22004-3781-4018-9a92-88958039248c, IInkStrokeDisp interface [Tablet PC],ScaleToRectangle method, IInkStrokeDisp.ScaleToRectangle, IInkStrokeDisp::ScaleToRectangle, ScaleToRectangle, ScaleToRectangle method [Tablet PC], ScaleToRectangle method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::ScaleToRectangle, tablet.iinkstrokedisp_scaletorectangle
f1_keywords:
- msinkaut/IInkStrokeDisp.ScaleToRectangle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkStrokeDisp.ScaleToRectangle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkStrokeDisp::ScaleToRectangle


## -description



Scales the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to fit in the specified <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.




## -parameters




### -param Rectangle [in]

The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> in ink space to which the stroke or collection of strokes is scaled. The strokes are scaled and translated to match the strokes' bounding box to the rectangle.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>
 

 

