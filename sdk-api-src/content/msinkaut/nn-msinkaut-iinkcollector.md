---
UID: NN:msinkaut.IInkCollector
title: IInkCollector (msinkaut.h)
author: windows-sdk-content
description: "."
old-location: tablet\iinkcollector.htm
tech.root: tablet
ms.assetid: 4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkCollector, IInkCollector interface [Tablet PC], IInkCollector interface [Tablet PC],described, msinkaut/IInkCollector, tablet.iinkcollector
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkCollector"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkCollector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCollector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCollector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCollector</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursorbuttondown">CursorButtonDown</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a> detects a cursor button that is down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursorbuttonup">CursorButtonUp</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> detects a cursor button that is up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a>
</td>
<td align="left" width="63%">
Occurs when the cursor tip contacts the digitizing tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a>
</td>
<td align="left" width="63%">
Occurs when a cursor enters the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a>
</td>
<td align="left" width="63%">
Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-doubleclick">DoubleClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-gesture">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application-specific gesture is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-mousedown">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object and a mouse button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-mousemove">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-mouseup">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object and a mouse button is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-mousewheel">MouseWheel</a>
</td>
<td align="left" width="63%">
Occurs when the mouse wheel moves while the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a>
</td>
<td align="left" width="63%">
Occurs when an in-air packet is seen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a>
</td>
<td align="left" width="63%">
Occurs when the ink collector receives a packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-stroke">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new stroke on any tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-systemgesture">SystemGesture</a>
</td>
<td align="left" width="63%">
Occurs when a system gesture is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-tabletadded">TabletAdded</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-tabletremoved">TabletRemoved</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> is removed from the system.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkCollector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest">GetEventInterest</a>
</td>
<td align="left" width="63%">
Retrieves the interest an object has in a particular event for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> class, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> class, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Indicates whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is interested in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle">GetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Gets the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Allows an ink collector (<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest">SetEventInterest</a>
</td>
<td align="left" width="63%">
Modifies a value that indicates whether an object or control has interest in a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the object or control in a known gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a>
</td>
<td align="left" width="63%">
Allows the ink collector (<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Sets the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCollector</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the desired packet description of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering">DynamicRendering</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets  a value that specifies whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object collects pen input (in-air packets, cursor in range events, and so on).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx">MarginX</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy">MarginY</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the custom mouse icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer">Renderer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object that is used to draw ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink">SupportHighContrastInk</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_tablet">Tablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets either the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.

</td>
</tr>
</table> 

