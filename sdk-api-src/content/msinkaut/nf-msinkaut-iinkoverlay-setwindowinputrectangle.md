---
UID: NF:msinkaut.IInkOverlay.SetWindowInputRectangle
title: IInkOverlay::SetWindowInputRectangle (msinkaut.h)
description: Sets the window rectangle, in pixels, within which ink is drawn. (IInkOverlay.SetWindowInputRectangle)
helpviewer_keywords: ["IInkOverlay","IInkOverlay interface [Tablet PC]","SetWindowInputRectangle method","IInkOverlay.SetWindowInputRectangle","IInkOverlay::SetWindowInputRectangle","SetWindowInputRectangle","SetWindowInputRectangle method [Tablet PC]","SetWindowInputRectangle method [Tablet PC]","IInkOverlay interface","b46139db-0473-4cd3-8f1b-d303f3430470","msinkaut/IInkOverlay::SetWindowInputRectangle","tablet.inkoverlay_setwindowinputrectangle"]
old-location: tablet\inkoverlay_setwindowinputrectangle.htm
tech.root: tablet
ms.assetid: 0f689b7d-0bcc-4cf2-8878-19f6af018b81
ms.date: 12/05/2018
ms.keywords: IInkOverlay, IInkOverlay interface [Tablet PC],SetWindowInputRectangle method, IInkOverlay.SetWindowInputRectangle, IInkOverlay::SetWindowInputRectangle, SetWindowInputRectangle, SetWindowInputRectangle method [Tablet PC], SetWindowInputRectangle method [Tablet PC],IInkOverlay interface, b46139db-0473-4cd3-8f1b-d303f3430470, msinkaut/IInkOverlay::SetWindowInputRectangle, tablet.inkoverlay_setwindowinputrectangle
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
 - IInkOverlay::SetWindowInputRectangle
 - msinkaut/IInkOverlay::SetWindowInputRectangle
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
 - IInkOverlay.SetWindowInputRectangle
---

# IInkOverlay::SetWindowInputRectangle


## -description

Sets the window rectangle, in pixels, within which ink is drawn.

## -parameters

### -param WindowInputRectangle [in]

The rectangle, in window coordinates, on which ink is drawn.

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
The rectangle coordinates are invalid (for example, width/height of 0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_COLLECTOR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
Cannot update mappings while in the middle of a stroke.

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
<dt><b>E_INK_OVERLAPPING_INPUT_RECT</b></dt>
</dl>
</td>
<td width="60%">
The window input rectangle overlaps with the window input rectangle of an enabled InkCollector.

</td>
</tr>
</table>

## -remarks

The E_INK_OVERLAPPING_INPUT_RECT error is returned if the window input rectangle of an enabled ink collector (set with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property) overlaps the window input rectangle of another enabled ink collector.

<div class="alert"><b>Note</b>  Overlap can occur without an error as long as only one of the input rectangles is enabled at any known time.</div>
<div> </div>
By default, the window input rectangle is set to {0,0,0,0}. This default rectangle maps to the size of the entire window.

To reset the window input rectangle to its default behavior (an empty rectangle with coordinates {0,0,0,0}), pass {0,0,0,0} in the call to <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle</a>, and not <b>NULL</b>.

You cannot pass in a rectangle where the value of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right</a> property is less than the value of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left</a> property; or where the value of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom</a> property is less than the value of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top</a> property. For example, a rectangle with parameters of {500, 500, 400, 400} is not valid.

<div class="alert"><b>Caution</b>  If you set the window input rectangle to overlap a splitter control or the borders of the window, unpredictable results may occur when the window is resized.</div>
<div> </div>
<div class="alert"><b>Note</b>  Calling this method within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>,<b> WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to <b>SC_HOTKEY</b> or <b>SC_TASKLIST</b>; and <b>WM_SYSKEYDOWN</b> (when processing Alt+TAB or Alt+ESC key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle">GetWindowInputRectangle Method</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
