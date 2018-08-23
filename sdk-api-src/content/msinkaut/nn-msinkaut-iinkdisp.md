---
UID: NN:msinkaut.IInkDisp
title: IInkDisp
author: windows-sdk-content
description: "."
old-location: tablet\iinkdisp.htm
old-project: tablet
ms.assetid: 85B683AA-D859-4717-8C61-C0EB4BBA5F61
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IInkDisp, IInkDisp interface [Tablet PC], IInkDisp interface [Tablet PC],described, msinkaut/IInkDisp, tablet.iinkdisp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkDisp
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDisp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkDisp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDisp</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46bbdb98-524f-4b4b-95c0-005e71d672f1">InkAdded</a>
</td>
<td align="left" width="63%">
Occurs when a stroke is added to the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59ada470-6620-411d-889e-882f41ccea3e">InkDeleted</a>
</td>
<td align="left" width="63%">
Occurs when a stroke is deleted from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkDisp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5a7cbbc-361c-4e99-af31-f7114eb5261b">AddStrokesAtRectangle</a>
</td>
<td align="left" width="63%">
Adds a specified <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">Strokes</a> collection into this <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object at a specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/755c74c4-417a-49b5-9f3d-9348c05ac850">CanPaste</a>
</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> can be converted to an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1027f79d-1398-4db5-ba62-f67edf8ec939">Clip</a>
</td>
<td align="left" width="63%">
Removes portions of an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that are outside a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad62c9b3-6df6-445b-9085-7cd5c4b6b31f">ClipboardCopy</a>
</td>
<td align="left" width="63%">
Copies the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to the Clipboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4e6a183-242a-40af-871b-43a0b177a27a">ClipboardCopyWithRectangle</a>
</td>
<td align="left" width="63%">
Copies the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects that are contained within the known rectangle to the Clipboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2760791-4238-45a9-a561-a48a55d6444b">ClipboardPaste</a>
</td>
<td align="left" width="63%">
Copies the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> from the Clipboard to the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3ec6b42-2b5d-459e-ba09-88c27b125c40">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/116c5746-61ad-4a47-a5e3-4675af87b0f1">CreateStroke</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object from an array of packet data input values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21e68151-38c9-414f-840c-c2687a05aea4">CreateStrokes</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection from existing <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac6579ec-20f7-4a20-8cb8-5f3a6119959d">DeleteStroke</a>
</td>
<td align="left" width="63%">
Deletes a <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbc11006-a434-46f8-a78c-3b67e35ed32a">DeleteStrokes</a>
</td>
<td align="left" width="63%">
Deletes an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection from the <a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes</a> collection of the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cb109e5-5193-4022-a3b1-ade9be1337e8">ExtractStrokes</a>
</td>
<td align="left" width="63%">
Specifies the strokes to extract from an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a> and cut or copy into a new <b>InkDisp Class</b>, by using the known collection of strokes to determine which strokes to extract.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b32467a8-a677-4a80-8029-d364e6e372c6">ExtractWithRectangle</a>
</td>
<td align="left" width="63%">
Cuts or copies strokes from an existing <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object and pastes them into a new <b>InkDisp</b> object, by using the known rectangle to determine which strokes to extract.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b60188e-3e4b-421a-9e34-3f6f2a70a71a">GetBoundingBox</a>
</td>
<td align="left" width="63%">
Retrieves the bounding box in ink space coordinates for either all of the strokes in an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, an individual stroke, or an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2025f728-cb08-4285-8584-c9ad537e58f2">HitTestCircle</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that are either completely inside or intersected by a known circle.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe88410d-e3e7-4899-b6fe-04e6eed98bbb">HitTestWithLasso</a>
</td>
<td align="left" width="63%">
Retrieves the strokes within a polyline selection area.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/401c4f62-a406-49ac-9911-91f815cde9c8">HitTestWithRectangle</a>
</td>
<td align="left" width="63%">
Retrieves the strokes that are contained within a specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e71e434-b055-4e45-b8fd-f9c1ac84d308">Load</a>
</td>
<td align="left" width="63%">
Populates a new <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object with known binary data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ccf201-dbc9-484f-8038-6a964d304287">NearestPoint</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> within the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is nearest to a known point, optionally providing the index of the nearest point and the distance to the stroke from the specified point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save</a>
</td>
<td align="left" width="63%">
Converts the ink to the specified <a href="https://msdn.microsoft.com/ecbf48ce-0394-4da1-9f5c-d2626545982c">InkPersistenceFormat</a>, saves the ink by using the specified <a href="https://msdn.microsoft.com/dac49948-3977-4952-a6c0-f54c4a0a2e36">InkPersistenceCompressionMode</a>, and returns the binary data in an array of bytes.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDisp</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/33425e5b-2ba0-4026-ab19-33579e7bb9f5">CustomStrokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of custom strokes to be persisted with the ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3399219f-96a5-4c66-8e41-89927ea1020d">Dirty</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether the strokes of an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a> object have been modified since the last time the ink was saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0272c1e9-d910-4a9a-9dee-9d875437ca99">ExtendedProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of application-defined data that are stored in an object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f58cb875-a2f1-44f4-b8be-f3dfe9643c46">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of strokes that are contained in an object or used to create an object.

</td>
</tr>
</table> 

