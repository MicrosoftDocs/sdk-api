---
UID: NN:msinkaut.IInkOverlay
title: IInkOverlay (msinkaut.h)
description: .
helpviewer_keywords: ["IInkOverlay","IInkOverlay interface [Tablet PC]","IInkOverlay interface [Tablet PC]","described","msinkaut/IInkOverlay","tablet.iinkoverlay"]
old-location: tablet\iinkoverlay.htm
tech.root: tablet
ms.assetid: ACE11946-113B-42EE-A3F1-0036B1DF8141
ms.date: 12/05/2018
ms.keywords: IInkOverlay, IInkOverlay interface [Tablet PC], IInkOverlay interface [Tablet PC],described, msinkaut/IInkOverlay, tablet.iinkoverlay
req.header: msinkaut.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay
 - msinkaut/IInkOverlay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkOverlay
---

# IInkOverlay interface


## -description

Represents an object that is useful for annotation scenarios where users are not concerned with performing recognition on ink but instead are interested in the size, shape, color, and position of the ink.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkOverlay</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkOverlay</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkOverlay</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-cursorbuttondown">CursorButtonDown</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a> detects a cursor button that is down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-cursorbuttonup">CursorButtonUp</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> detects a cursor button that is up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-cursordown">CursorDown</a>
</td>
<td align="left" width="63%">
Occurs when the cursor tip contacts the digitizing tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-cursorinrange">CursorInRange</a>
</td>
<td align="left" width="63%">
Occurs when a cursor enters the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-cursoroutofrange">CursorOutOfRange</a>
</td>
<td align="left" width="63%">
Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-doubleclick">DoubleClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-gesture">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application-specific gesture is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-mousedown">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object and a mouse button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-mousemove">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-mouseup">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object and a mouse button is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-mousewheel">MouseWheel</a>
</td>
<td align="left" width="63%">
Occurs when the mouse wheel moves while the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-newinairpackets">NewInAirPackets</a>
</td>
<td align="left" width="63%">
Occurs when an in-air packet is seen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-newpackets">NewPackets</a>
</td>
<td align="left" width="63%">
Occurs when the ink collecto rreceives a packet

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-painted">Painted</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has completed redrawing itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-painting">Painting</a>
</td>
<td align="left" width="63%">
Occurs before the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> has completed redrawing itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionchanged">SelectionChanged</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionchanging">SelectionChanging</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionmoved">SelectionMoved</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionmoving">SelectionMoving</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionresized">SelectionResized</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-selectionresizing">SelectionResizing</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-stroke">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new stroke on any tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-strokesdeleted">StrokesDeleted</a>
</td>
<td align="left" width="63%">
Occurs after strokes have been deleted from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-strokesdeleting">StrokesDeleting</a>
</td>
<td align="left" width="63%">
Occurs before strokes are deleted from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-systemgesture">SystemGesture</a>
</td>
<td align="left" width="63%">
Occurs when a system gesture  is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-tabletadded">TabletAdded</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkoverlay-tabletremoved">TabletRemoved</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is removed from the system.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkOverlay</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw">Draw</a>
</td>
<td align="left" width="63%">
Sets a rectangle in which to redraw the ink within the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-geteventinterest">GetEventInterest</a>
</td>
<td align="left" width="63%">
Retrieves the interest an object has in a particular event for the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> class, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> class, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-getgesturestatus">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is interested in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-getwindowinputrectangle">GetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Gets the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection">HitTestSelection</a>
</td>
<td align="left" width="63%">
Determines what portion of the selection was hit during a hit test.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-setalltabletsmode">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Allows an ink collector  (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-seteventinterest">SetEventInterest</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether an object or control has interest in a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-setgesturestatus">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Sets the interest of the object or control in a known gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a>
</td>
<td align="left" width="63%">
Allows the ink collector  (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-setwindowinputrectangle">SetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Sets the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkOverlay</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode">AttachMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is attached behind or in front of the known window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_autoredraw">AutoRedraw</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_collectingink">CollectingInk</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_collectionmode">CollectionMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_cursors">Cursors</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_defaultdrawingattributes">DefaultDrawingAttributes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the default drawing attributes to use when drawing and displaying ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_desiredpacketdescription">DesiredPacketDescription</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the desired packet description of the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether ink is rendered as it is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object collects pen input (in-air packets, cursor in range events, and so on).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode">EraserMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether ink is erased by stroke or by point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth">EraserWidth</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies the width of the eraser pen tip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd">hWnd</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the handle value of the window on which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink">Ink</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or an <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_marginx">MarginX</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the x-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_marginy">MarginY</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the y-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_mouseicon">MouseIcon</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the custom mouse icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_mousepointer">MousePointer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates the type of mouse pointer that appears.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_renderer">Renderer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object that is used to draw ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection">Selection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that is currently selected inside the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastink">SupportHighContrastInk</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui">SupportHighContrastSelectionUI</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_tablet">Tablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets either the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.

</td>
</tr>
</table>

## -remarks

Creating the InkOverlay control behind a transparent control (such as a GroupBox with the WS_EX_TRANSPARENT property set) will prevent InkOverlay from collecting ink.

## -see-also

[IInkCollector interface](nn-msinkaut-iinkcollector.md), [IInkOverlay interface](nn-msinkaut-iinkoverlay.md), [InkOverlay class](/windows/win32/tablet/inkoverlay-class)