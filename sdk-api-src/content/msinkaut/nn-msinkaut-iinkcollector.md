---
UID: NN:msinkaut.IInkCollector
title: IInkCollector
author: windows-sdk-content
description: "."
old-location: tablet\iinkcollector.htm
tech.root: tablet
ms.assetid: 4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IInkCollector, IInkCollector interface [Tablet PC], IInkCollector interface [Tablet PC],described, msinkaut/IInkCollector, tablet.iinkcollector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCollector interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCollector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkCollector</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/65e7f68b-f911-4634-b850-178eb6eaf86e">CursorButtonDown</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a> detects a cursor button that is down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f07daad7-e0d1-45cf-a708-5486a5dfda8b">CursorButtonUp</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> detects a cursor button that is up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf914849-ef33-4746-b2e1-c768cd1d87aa">CursorDown</a>
</td>
<td align="left" width="63%">
Occurs when the cursor tip contacts the digitizing tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange</a>
</td>
<td align="left" width="63%">
Occurs when a cursor enters the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3a570ed-570b-4579-b120-ed5457630bc2">CursorOutOfRange</a>
</td>
<td align="left" width="63%">
Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48c3a695-0ec4-46ea-b1ea-a846e39d53ec">DoubleClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application-specific gesture is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db9ec396-b2a7-4f4f-99f2-95aad46eea28">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object and a mouse button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/688ac7ef-dcee-44a4-8947-117966365061">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dcc6c68-89f7-4020-b378-56df9d46974b">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object and a mouse button is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/418cf67c-0ec0-49e3-a17f-9eaeb40bb602">MouseWheel</a>
</td>
<td align="left" width="63%">
Occurs when the mouse wheel moves while the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8eacdec-0381-435f-b453-24dca1c507c9">NewInAirPackets</a>
</td>
<td align="left" width="63%">
Occurs when an in-air packet is seen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2682e7ba-dabd-497e-aea4-6d3f837f4f10">NewPackets</a>
</td>
<td align="left" width="63%">
Occurs when the ink collector receives a packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new stroke on any tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11071d6f-8aa3-4902-94fd-89ad0cf17729">SystemGesture</a>
</td>
<td align="left" width="63%">
Occurs when a system gesture is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5f90fce-faf7-411b-a4d6-deb5d0f22f4a">TabletAdded</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> is added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/659a9809-fe35-4d34-aa95-af353998c350">TabletRemoved</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> is removed from the system.

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
<a href="https://msdn.microsoft.com/532a798e-b434-4730-8c20-7ec60255f170">GetEventInterest</a>
</td>
<td align="left" width="63%">
Retrieves the interest an object has in a particular event for the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> class, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> class, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31973709-1702-4ec1-8228-b0d1bdb64bc8">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object is interested in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c">GetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Gets the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Allows an ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df25efbb-5229-4211-948f-3a213154a967">SetEventInterest</a>
</td>
<td align="left" width="63%">
Modifies a value that indicates whether an object or control has interest in a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bab227f-d095-48e8-856f-6446e62826dd">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the object or control in a known gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode</a>
</td>
<td align="left" width="63%">
Allows the ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b46139db-0473-4cd3-8f1b-d303f3430470">SetWindowInputRectangle</a>
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

<a href="https://msdn.microsoft.com/f5cb889e-75db-416e-9754-a96f65dad6ed">AutoRedraw</a>


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

<a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/390fa1a1-254a-4070-806c-c8c478f69254">CollectionMode</a>


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

<a href="https://msdn.microsoft.com/6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4">Cursors</a>


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

<a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a>


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

<a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the desired packet description of the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48464ebc-d1a2-4068-b9ee-061adce30879">DynamicRendering</a>


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

<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets  a value that specifies whether the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object collects pen input (in-air packets, cursor in range events, and so on).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a>


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

<a href="https://msdn.microsoft.com/62881a0e-3932-49a1-8e7d-3e74474f2214">Ink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is associated with an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or an <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d128fb84-f3cb-4e10-8764-ccb060841383">MarginX</a>


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

<a href="https://msdn.microsoft.com/6cba076e-6392-4f0a-a80d-3df903d0ba13">MarginY</a>


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

<a href="https://msdn.microsoft.com/9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4">MouseIcon</a>


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

<a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer</a>


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

<a href="https://msdn.microsoft.com/1abd8f85-88f5-4dc6-a0b8-9156b57c57a5">Renderer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object that is used to draw ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk</a>


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

<a href="https://msdn.microsoft.com/170c3b43-6472-465b-bb09-22ba1a68c6e0">Tablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets either the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.

</td>
</tr>
</table> 

