---
UID: NN:msinkaut.IInkPicture
title: IInkPicture
author: windows-sdk-content
description: "."
old-location: tablet\iinkpicture.htm
tech.root: tablet
ms.assetid: EA6AC3DD-5F13-442A-B93D-FF0A5333609A
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IInkPicture, IInkPicture interface [Tablet PC], IInkPicture interface [Tablet PC],described, msinkaut/IInkPicture, tablet.iinkpicture
ms.prod: windows
ms.technology: windows-sdk
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
 - IInkPicture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkPicture</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkPicture</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/326bac37-2d5d-434b-916c-8a675bab5052">Click</a>
</td>
<td align="left" width="63%">
Occurs when a user clicks the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ee2c19e-8a44-428b-a4c1-3c7250dcdeda">CursorButtonDown</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a> detects a cursor button that is down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb10b032-a88d-4b52-9062-c0b63dfe98e9">CursorButtonUp</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> detects a cursor button that is up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d524400-1341-45da-86b2-098e34ed5a1c">CursorDown</a>
</td>
<td align="left" width="63%">
Occurs when the cursor tip contacts the digitizing tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e921e175-a2cf-45e6-bb81-dc82e384d3b1">CursorInRange</a>
</td>
<td align="left" width="63%">
Occurs when a cursor enters the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c71a4ad-3c09-4134-b0e7-82f29e8913ed">CursorOutOfRange</a>
</td>
<td align="left" width="63%">
Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b2a6413-d415-4bf1-a291-35f4c3c5a0dc">DblClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a20f2d78-6cfe-4755-968e-91369021db1b">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application-specific <i>gesture</i> is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d83823ea-d863-4eb7-8f6b-fa7a3396e64b">KeyDown</a>
</td>
<td align="left" width="63%">
Occurs when a key is pressed and in the down position while the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb61eff-a92c-40b0-940c-02e14cd34e5f">KeyPress</a>
</td>
<td align="left" width="63%">
Occurs when a key is pressed while the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e22633b5-40fe-4b94-a660-684c4f5c96f3">KeyUp</a>
</td>
<td align="left" width="63%">
Occurs when a key is released while the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff776b2b-7dd8-4d3d-b0f6-714b186d447e">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is over the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control and a mouse button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb31bf2f-e889-4da3-b408-e5612e2af95b">MouseEnter</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer enters the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a03833-529e-4fca-b8df-ae7edefc8e5e">MouseHover</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer hovers over the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b7961cd-58a3-4e75-bb9e-fbb6dc225d3d">MouseLeave</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer leaves the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4c703da-0e4a-4d4c-9a6c-0e002344fb2f">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e49acc8-1ce1-45ff-b87c-04bdc653156a">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the mouse pointer is moved over the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control and a mouse button is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f56a8af9-7618-4fa3-8dd5-aa81a7f817e4">MouseWheel</a>
</td>
<td align="left" width="63%">
Occurs when the mouse wheel moves while the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30bc423d-0642-4515-9e51-a8b8b36aecad">NewInAirPackets</a>
</td>
<td align="left" width="63%">
Occurs when an in-air packet is seen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d120198-c016-4452-b8a8-22c4ad87d526">NewPackets</a>
</td>
<td align="left" width="63%">
Occurs when the ink collector receives a packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8194cff-ed94-402e-8564-08d370f958b4">Painted</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has completed redrawing itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb">Painting</a>
</td>
<td align="left" width="63%">
Occurs before the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control redraws itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/436db420-f9ea-46f1-b922-c8663371edd5">Resize</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is resized (when the Width and/or Height property values change).


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e300ec91-e8f3-473f-b526-efeafafaa32a">SelectionChanged</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ae30ff-fb0d-44cc-a5d3-295117addafd">SelectionChanging</a>
</td>
<td align="left" width="63%">
Occurs when the selection of ink within the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/669dc6c2-1620-40f3-b4b5-7ab8967e739a">SelectionMoved</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310003a1-f282-4efa-9a75-c575a9193a77">SelectionMoving</a>
</td>
<td align="left" width="63%">
Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e7f461f-2909-40ab-98d8-b763d489eb62">SelectionResized</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da708712-2773-45f5-9d9b-49fabe7fdb5a">SelectionResizing</a>
</td>
<td align="left" width="63%">
Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the <a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5fc6c82-f9c8-4104-8abe-082c47c56be9">SizeChanged</a>
</td>
<td align="left" width="63%">
Occurs after the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has been resized, specifically, after the <a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width</a> or <a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height</a> property value changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae56b5a2-e3e2-468c-a572-a9b46eb1d39d">SizeModeChanged</a>
</td>
<td align="left" width="63%">
Occurs after the <a href="https://msdn.microsoft.com/3ce10b92-80d4-4517-92cb-eff10fc8c0ba">SizeMode</a> property of the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has been changed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2829b65a-6120-402e-91e3-5587d1f456f9">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new stroke on any tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/577ad52b-ecd3-4a49-8997-481ebdb47203">StrokesAdded</a>
</td>
<td align="left" width="63%">
Occurs when one or more <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects are added to the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/395544e1-dc93-45d3-ac7a-d54712f3c027">StrokesDeleted</a>
</td>
<td align="left" width="63%">
Occurs after <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects have been deleted from the <a href="https://msdn.microsoft.com/8a6001bb-cfb9-4c24-8f99-3c8f0acd443c">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/747e0fdf-c68b-4805-bdc8-aa05e95ec0f7">StrokesDeleting</a>
</td>
<td align="left" width="63%">
Occurs before <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects are deleted from the <a href="https://msdn.microsoft.com/8a6001bb-cfb9-4c24-8f99-3c8f0acd443c">Ink</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d77c24a-dc01-4ea0-b142-e83b1023acc1">SystemColorsChanged</a>
</td>
<td align="left" width="63%">
Occurs after the system colors change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36e2ac5a-dc91-47c2-a8e5-e555437c0a5d">SystemGesture</a>
</td>
<td align="left" width="63%">
Occurs when a system gesture  is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5df10efd-7055-43fa-881f-67eb5fd6adcf">TabletAdded</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> is added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a4640a7-cbd9-4304-88c6-86036423628d">TabletRemoved</a>
</td>
<td align="left" width="63%">
Occurs when a <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> is removed from the system.

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
<a href="https://msdn.microsoft.com/e025a118-acf1-4b52-ace9-85a3a5a558fa">GetEventInterest</a>
</td>
<td align="left" width="63%">
Retrieves the interest an object has in a particular event for the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> class, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> class, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4ccc35d-35b5-4633-acc9-efd4c7eb05e3">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control has interest in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/975e5921-cc76-4b38-9f3c-364e8704ba03">GetWindowInputRectangle</a>
</td>
<td align="left" width="63%">
Retrieves the window rectangle, in pixels, within which ink is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dc745d8-7e2a-4255-86c6-226bf82d3d64">HitTestSelection</a>
</td>
<td align="left" width="63%">
Retrieves a member of the <a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult</a> enumeration, which specifies which part of a selection, if any, was hit during a hit test.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Allows an ink collector  (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from any tablet attached to the Tablet PC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4baaf348-dec7-4b81-8415-b9f4ace14f5d">SetEventInterest</a>
</td>
<td align="left" width="63%">
Modifies a value that indicates whether an object or control has interest in a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36f3611a-c7d9-49a2-9ead-db98647f6da7">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the object or control in a known gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode</a>
</td>
<td align="left" width="63%">
Allows the ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3602a550-d37b-4a78-b949-04f5e3cb923a">SetWindowInputRectangle</a>
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

<a href="https://msdn.microsoft.com/8dea3bee-c0d9-488e-834f-6a70d4deaf34">AutoRedraw</a>


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

<a href="https://msdn.microsoft.com/f97858c5-a8f9-4d92-9ed2-bdeaeb1e2f5a">BackColor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the background color for the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/19fbe26e-02a4-4d05-a2e8-25d2f8ae1146">CollectingInk</a>


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

<a href="https://msdn.microsoft.com/fe3d1158-b99b-4ae1-a509-c6f34b42615f">CollectionMode</a>


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

<a href="https://msdn.microsoft.com/815f4895-d418-4336-9420-2405bcd5cfb3">Cursors</a>


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

<a href="https://msdn.microsoft.com/c3f817be-28ed-4eec-a30d-98ad8e39853b">CustomStrokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection to be persisted with the ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9a4dff66-9789-4979-947e-73bbf85cece2">DefaultDrawingAttributes</a>


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

<a href="https://msdn.microsoft.com/5b4a667a-b927-4278-9be2-2d7163568582">DesiredPacketDescription</a>


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

<a href="https://msdn.microsoft.com/e1200e66-d2d7-4c82-b243-53618a3699ae">DynamicRendering</a>


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

<a href="https://msdn.microsoft.com/5767f768-d59c-404e-9098-ab5e0c427c7d">EditingMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control can respond to user-generated events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f6471163-8209-4dd0-887c-0edd54ebb50e">EraserMode</a>


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

<a href="https://msdn.microsoft.com/8a880a9a-acd4-4cb1-aea7-4d834ecd9490">EraserWidth</a>


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

<a href="https://msdn.microsoft.com/c11f13f5-f0a8-45f8-83c2-372df670ef1f">hWnd</a>


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

<a href="https://msdn.microsoft.com/8a6001bb-cfb9-4c24-8f99-3c8f0acd443c">Ink</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is associated with the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c463debc-341b-4491-8543-70623bf717d0">MarginX</a>


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

<a href="https://msdn.microsoft.com/f5320061-36c7-4dcb-b5d3-3df41ddcac2a">MarginY</a>


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

<a href="https://msdn.microsoft.com/a095dca7-4dc9-4661-8c78-0e357a57f982">MouseIcon</a>


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

<a href="https://msdn.microsoft.com/94536770-01ef-41c5-9217-0aa2ef9c36ac">MousePointer</a>


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

<a href="https://msdn.microsoft.com/c07433f2-d32c-4b6f-ad15-6b49dc6f4efa">Picture</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets the graphics file to appear on the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5df5918a-caca-4296-8464-3710ff904b10">Renderer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object that is used to draw ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/29d54781-b83b-4733-95fe-86577958e0d1">Selection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that is currently selected inside the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ce10b92-80d4-4517-92cb-eff10fc8c0ba">SizeMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets how the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control handles image placement and sizing.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f57e1fe-8224-43ef-bd26-2d15da625725">SupportHighContrastInk</a>


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

<a href="https://msdn.microsoft.com/f522a998-89f0-4d8d-bb19-949d62f5a786">SupportHighContrastSelectionUI</a>


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

<a href="https://msdn.microsoft.com/b3fbfec6-dba8-43bd-b3b0-7c435a2cf407">Tablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets either the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.

</td>
</tr>
</table> 

