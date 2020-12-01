---
UID: NN:msinkaut.IInkPicture
title: IInkPicture (msinkaut.h)
description: .
helpviewer_keywords: ["IInkPicture","IInkPicture interface [Tablet PC]","IInkPicture interface [Tablet PC]","described","msinkaut/IInkPicture","tablet.iinkpicture"]
old-location: tablet\iinkpicture.htm
tech.root: tablet
ms.assetid: EA6AC3DD-5F13-442A-B93D-FF0A5333609A
ms.date: 03/25/2020
ms.keywords: IInkPicture, IInkPicture interface [Tablet PC], IInkPicture interface [Tablet PC],described, msinkaut/IInkPicture, tablet.iinkpicture
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
 - IInkPicture
 - msinkaut/IInkPicture
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
 - IInkPicture
---

# IInkPicture interface


## -description

Represents an object that provides the ability to place an image in an application for users to add ink on top of. It is intended for scenarios in which ink is not recognized as text but is instead stored as ink.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkPicture</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkPicture</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkPicture</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-click">Click</a>
</td>
<td align="left" width="63%">
Occurs when a user clicks the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-cursorbuttondown">CursorButtonDown</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a> detects a cursor button that is down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-cursorbuttonup">CursorButtonUp</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> detects a cursor button that is up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-cursordown">CursorDown</a>
</td>
<td align="left" width="63%">
Occurs when the cursor tip contacts the digitizing tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-cursorinrange">CursorInRange</a>
</td>
<td align="left" width="63%">
Occurs when a cursor enters the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-cursoroutofrange">CursorOutOfRange</a>
</td>
<td align="left" width="63%">
Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-dblclick">DblClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-gesture">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application-specific <i>gesture</i> is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-keydown">KeyDown</a>
</td>
<td align="left" width="63%">
Occurs when a key is pressed and in the down position while the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-keypress">KeyPress</a>
</td>
<td align="left" width="63%">
Occurs when a key is pressed while the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-keyup">KeyUp</a>
</td>
<td align="left" width="63%">
Occurs when a key is released while the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mousedown">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control and a mouse button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mouseenter">MouseEnter</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer enters the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mousehover">MouseHover</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer hovers over the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mouseleave">MouseLeave</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer leaves the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mousemove">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mouseup">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control and a mouse button is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-mousewheel">MouseWheel</a>
</td>
<td align="left" width="63%">
Occurs when the mouse wheel moves while the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-newinairpackets">NewInAirPackets</a>
</td>
<td align="left" width="63%">
Occurs when an in-air packet is seen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-newpackets">NewPackets</a>
</td>
<td align="left" width="63%">
Occurs when the ink collector receives a packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-painted">Painted</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has completed redrawing itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-painting">Painting</a>
</td>
<td align="left" width="63%">
Occurs before the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control redraws itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-resize">Resize</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is resized (when the Width and/or Height property values change).


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionchanged">SelectionChanged</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionchanging">SelectionChanging</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionmoved">SelectionMoved</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionmoving">SelectionMoving</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionresized">SelectionResized</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-selectionresizing">SelectionResizing</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-sizechanged">SizeChanged</a>
</td>
<td align="left" width="63%">
Occurs after the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has been resized, specifically, after the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width</a> or <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height</a> property value changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-sizemodechanged">SizeModeChanged</a>
</td>
<td align="left" width="63%">
Occurs after the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode">SizeMode</a> property of the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has been changed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-stroke">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new stroke on any tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-strokesadded">StrokesAdded</a>
</td>
<td align="left" width="63%">
Occurs when one or more <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects are added to the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-strokesdeleted">StrokesDeleted</a>
</td>
<td align="left" width="63%">
Occurs after <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects have been deleted from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-strokesdeleting">StrokesDeleting</a>
</td>
<td align="left" width="63%">
Occurs before <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects are deleted from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-systemcolorschanged">SystemColorsChanged</a>
</td>
<td align="left" width="63%">
Occurs after the system colors change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-systemgesture">SystemGesture</a>
</td>
<td align="left" width="63%">
Occurs when a system gesture  is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-tabletadded">TabletAdded</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/tablet/inkpicture-tabletremoved">TabletRemoved</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is removed from the system.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkPicture</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest">GetEventInterest</a>
</td>
<td align="left" width="63%">
Retrieves the interest an object has in a particular event for the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> class, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> class, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has interest in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle">GetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Retrieves the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection">HitTestSelection</a>
</td>
<td align="left" width="63%">
Retrieves a member of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult">SelectionHitResult</a> enumeration, which specifies which part of a selection, if any, was hit during a hit test.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Allows an ink collector  (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest">SetEventInterest</a>
</td>
<td align="left" width="63%">
Modifies a value that indicates whether an object or control has interest in a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the object or control in a known gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a>
</td>
<td align="left" width="63%">
Allows the ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle">SetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Modifies the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkPicture</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw">AutoRedraw</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether an ink collectcor  repaints the ink when the window is invalidated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor">BackColor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the background color for the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink">CollectingInk</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode">CollectionMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the collection mode that determines whether ink, gestures, or both are recognized as the user writes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors">Cursors</a>


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

<a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)">CustomStrokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection to be persisted with the ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes">DefaultDrawingAttributes</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription">DesiredPacketDescription</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering">DynamicRendering</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode">EditingMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode">EraserMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether ink is erased by stroke or by point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth">EraserWidth</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies the width of the eraser pen tip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd">hWnd</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink">Ink</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx">MarginX</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy">MarginY</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon">MouseIcon</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer">MousePointer</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture">Picture</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets the graphics file to appear on the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer">Renderer</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection">Selection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that is currently selected inside the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode">SizeMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets how the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control handles image placement and sizing.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink">SupportHighContrastInk</a>


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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui">SupportHighContrastSelectionUI</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether all selection user interface (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet">Tablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets either the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.

</td>
</tr>
</table>

## -see-also

[InkPicture Control](/windows/win32/tablet/inkpicture-control-reference)