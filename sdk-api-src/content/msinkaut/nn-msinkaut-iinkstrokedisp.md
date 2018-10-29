---
UID: NN:msinkaut.IInkStrokeDisp
title: IInkStrokeDisp
author: windows-sdk-content
description: Represents a single ink stroke.A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark.
old-location: tablet\iinkstrokedisp.htm
tech.root: tablet
ms.assetid: b18464ba-feb6-4bb5-9fcf-82feff9bcce4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], IInkStrokeDisp interface [Tablet PC],described, b18464ba-feb6-4bb5-9fcf-82feff9bcce4, msinkaut/IInkStrokeDisp, tablet.iinkstrokedisp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IInkStrokeDisp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokeDisp interface


## -description



Represents a single ink stroke.

A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark. It is the set of data that is captured in a single pen down, up, or move sequence.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokeDisp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkStrokeDisp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkStrokeDisp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3733613-fc8e-41f2-9172-07b61fc133dd">Clip</a>
</td>
<td align="left" width="63%">
Removes the portions of the <b>IInkStrokeDisp</b> that are outside a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a070fc87-608c-47be-b9b2-e2a41a31226f">FindIntersections</a>
</td>
<td align="left" width="63%">
Finds the points where this <b>IInkStrokeDisp</b> intersects other strokes within an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

This method can determine only the points of intersection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b2c8cfc-05e6-4b53-b709-72291ee78471">GetBoundingBox</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle, in ink space coordinates, that corresponds to the portion of the display to invalidate or redraw when displaying an <b>IInkStrokeDisp</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e39e3fc3-bcdc-4d88-8051-18ed8b183c79">GetFlattenedBezierPoints</a>
</td>
<td align="left" width="63%">
Retrieves the array of actual points that are used to approximate the Bezier representation of a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/015ca2ca-3bcc-443c-a38c-7f67b69c5907">GetPacketData</a>
</td>
<td align="left" width="63%">
Retrieves the packet data associated with one or more points in an <b>IInkStrokeDisp</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21b13777-d924-45d6-bdcc-284c9b7d9627">GetPacketDescriptionPropertyMetrics</a>
</td>
<td align="left" width="63%">
Retrieves the metrics for a given packet description type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/135dcd06-f533-4470-b5b0-ea559c20e3c4">GetPacketValuesByProperty</a>
</td>
<td align="left" width="63%">
Retrieves the data for a known packet property from one or more packets in the <b>IInkStrokeDisp</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76378521-15d1-48a0-ae9f-8362faf60c9f">GetPoints</a>
</td>
<td align="left" width="63%">
Retrieves the points that make up a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe042e12-21fa-4dae-988c-d082aa867520">GetRectangleIntersections</a>
</td>
<td align="left" width="63%">
Finds the points where a stroke intersects a given rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b87a1bc0-b17b-419b-947e-48746f4903e8">HitTestCircle</a>
</td>
<td align="left" width="63%">
Determines whether a stroke is either completely inside or intersected by a given circle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d3425c0-6000-4478-9c67-5fdb8e2316e5">Move</a>
</td>
<td align="left" width="63%">
Applies a translation to the ink of the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87c01f9d-b48a-459c-99f8-9634e1693fa0">NearestPoint</a>
</td>
<td align="left" width="63%">
Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b3d5a58-31e8-4d0e-a1c9-25bb36bb8d9c">Rotate</a>
</td>
<td align="left" width="63%">
Rotates the ink using an angle in degrees around a center point of the rotation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bc22004-3781-4018-9a92-88958039248c">ScaleToRectangle</a>
</td>
<td align="left" width="63%">
Scales the stroke to fit in the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4140abe-adc8-492d-bb8c-96fba5ca3bd0">ScaleTransform</a>
</td>
<td align="left" width="63%">
Scales the ink using X and Y factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d90e93e-4c4a-43bd-a431-59522e332f2a">SetPacketValuesByProperty</a>
</td>
<td align="left" width="63%">
Sets the packet values for a particular property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/759e3195-e1de-45eb-a9de-8ec8fe2347c1">SetPoints</a>
</td>
<td align="left" width="63%">
Sets the points of the stroke using an array of X, Y values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/887dd883-1a24-4a78-8f08-f4cd45bf4840">Shear</a>
</td>
<td align="left" width="63%">
Shears the ink in the stroke by the specified horizontal and vertical factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ae627e9-c546-485a-880c-e59d2191884d">Split</a>
</td>
<td align="left" width="63%">
Splits the stroke at the specified location on the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7860215-a267-407e-9105-8e51340f4216">Transform</a>
</td>
<td align="left" width="63%">
Applies a linear transformation to a stroke, which can represent scaling, rotation, translation, and combinations of transformations.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokeDisp</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9fdd007a-1c8e-4389-975c-849a67be94a1">BezierCusps</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an array that contains the indices of the cusps of the Bezier approximation of the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/76bb749d-76cd-4c40-add3-4065d46ed6cb">BezierPoints</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the array of control points that represent the Bezier approximation of the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d34eaf9d-ad2a-4bf7-ac6d-ed4b19134a50">Deleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that indicates whether the <b>IInkStrokeDisp</b> object has been deleted from its parent <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f41de939-0c20-4128-bee4-22a0c434159f">DrawingAttributes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the drawing attributes to apply to ink as it is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6263770e-741d-4b4f-b33f-f808b7816622">ExtendedProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of application-defined data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f8e9d2b2-c3d1-4ea8-aed6-649bf6d4d353">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the identifier of the <b>IInkStrokeDisp</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/46283c0a-0280-4bd9-a6f1-2aa943b8b1b5">Ink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the parent <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object for this stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f7cd47f8-809b-455d-873f-81dba80549b9">PacketCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of packets received for a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c81f14e2-d97f-42cd-8498-240f8d39f9bc">PacketDescription</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an array of globally unique identifiers (GUIDs) that describes the types of packet data stored in the Stroke object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42016aa0-7cc4-43d5-a055-7007a4bf9f07">PacketSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the size, in bytes, of a packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/67ae7265-4416-4eef-8a8f-85f3a5751200">PolylineCusps</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an array that contains the indices of the cusps of the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d3b97071-d0bd-4910-93a4-409241e427eb">SelfIntersections</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the self-intersections of the stroke.

</td>
</tr>
</table> 


## -remarks



If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

