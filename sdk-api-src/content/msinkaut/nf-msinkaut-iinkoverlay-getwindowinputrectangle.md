---
UID: NF:msinkaut.IInkOverlay.GetWindowInputRectangle
title: IInkOverlay::GetWindowInputRectangle (msinkaut.h)
description: Gets the window rectangle, in pixels, within which ink is drawn. (IInkOverlay.GetWindowInputRectangle)
helpviewer_keywords: ["0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c","GetWindowInputRectangle","GetWindowInputRectangle method [Tablet PC]","GetWindowInputRectangle method [Tablet PC]","IInkOverlay interface","IInkOverlay","IInkOverlay interface [Tablet PC]","GetWindowInputRectangle method","IInkOverlay.GetWindowInputRectangle","IInkOverlay::GetWindowInputRectangle","msinkaut/IInkOverlay::GetWindowInputRectangle","tablet.inkoverlay_getwindowinputrectangle"]
old-location: tablet\inkoverlay_getwindowinputrectangle.htm
tech.root: tablet
ms.assetid: e0e4cabe-f8f1-48b5-a12a-789b7c9c5973
ms.date: 12/05/2018
ms.keywords: 0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c, GetWindowInputRectangle, GetWindowInputRectangle method [Tablet PC], GetWindowInputRectangle method [Tablet PC],IInkOverlay interface, IInkOverlay, IInkOverlay interface [Tablet PC],GetWindowInputRectangle method, IInkOverlay.GetWindowInputRectangle, IInkOverlay::GetWindowInputRectangle, msinkaut/IInkOverlay::GetWindowInputRectangle, tablet.inkoverlay_getwindowinputrectangle
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
 - IInkOverlay::GetWindowInputRectangle
 - msinkaut/IInkOverlay::GetWindowInputRectangle
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
 - IInkOverlay.GetWindowInputRectangle
---

# IInkOverlay::GetWindowInputRectangle


## -description

Gets the window rectangle, in pixels, within which ink is drawn.

## -parameters

### -param WindowInputRectangle [out]

The rectangle, of type <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a>, on which ink is drawn.

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The InkRectangle object is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurs inside the method.

</td>
</tr>
</table>

## -remarks

You must first allocate the rectangle before passing it on to this method.

By default, the window input rectangle is set to {0,0,0,0}. This default rectangle maps to the size of the entire window.

If you call <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle">GetWindowInputRectangle</a> before you call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle</a> method, this method gets a rectangle with the default coordinates.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle Method</a>
