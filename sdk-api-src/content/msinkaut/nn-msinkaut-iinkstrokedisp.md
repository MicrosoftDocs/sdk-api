---
UID: NN:msinkaut.IInkStrokeDisp
title: IInkStrokeDisp (msinkaut.h)
description: Represents a single ink stroke.A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark.
old-location: tablet\iinkstrokedisp.htm
tech.root: tablet
ms.assetid: b18464ba-feb6-4bb5-9fcf-82feff9bcce4
ms.date: 12/05/2018
ms.keywords: IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], IInkStrokeDisp interface [Tablet PC],described, b18464ba-feb6-4bb5-9fcf-82feff9bcce4, msinkaut/IInkStrokeDisp, tablet.iinkstrokedisp
f1_keywords:
- msinkaut/IInkStrokeDisp
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
- IInkStrokeDisp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkStrokeDisp interface


## -description



Represents a single ink stroke.

A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark. It is the set of data that is captured in a single pen down, up, or move sequence.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkStrokeDisp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkStrokeDisp</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip">Clip</a>
</td>
<td align="left" width="63%">
Removes the portions of the <b>IInkStrokeDisp</b> that are outside a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-findintersections">FindIntersections</a>
</td>
<td align="left" width="63%">
Finds the points where this <b>IInkStrokeDisp</b> intersects other strokes within an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

This method can determine only the points of intersection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox">GetBoundingBox</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle, in ink space coordinates, that corresponds to the portion of the display to invalidate or redraw when displaying an <b>IInkStrokeDisp</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getflattenedbezierpoints">GetFlattenedBezierPoints</a>
</td>
<td align="left" width="63%">
Retrieves the array of actual points that are used to approximate the Bezier representation of a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdata">GetPacketData</a>
</td>
<td align="left" width="63%">
Retrieves the packet data associated with one or more points in an <b>IInkStrokeDisp</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics</a>
</td>
<td align="left" width="63%">
Retrieves the metrics for a given packet description type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty">GetPacketValuesByProperty</a>
</td>
<td align="left" width="63%">
Retrieves the data for a known packet property from one or more packets in the <b>IInkStrokeDisp</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpoints">GetPoints</a>
</td>
<td align="left" width="63%">
Retrieves the points that make up a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getrectangleintersections">GetRectangleIntersections</a>
</td>
<td align="left" width="63%">
Finds the points where a stroke intersects a given rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-hittestcircle">HitTestCircle</a>
</td>
<td align="left" width="63%">
Determines whether a stroke is either completely inside or intersected by a given circle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-move">Move</a>
</td>
<td align="left" width="63%">
Applies a translation to the ink of the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-nearestpoint">NearestPoint</a>
</td>
<td align="left" width="63%">
Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-rotate">Rotate</a>
</td>
<td align="left" width="63%">
Rotates the ink using an angle in degrees around a center point of the rotation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletorectangle">ScaleToRectangle</a>
</td>
<td align="left" width="63%">
Scales the stroke to fit in the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform">ScaleTransform</a>
</td>
<td align="left" width="63%">
Scales the ink using X and Y factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty">SetPacketValuesByProperty</a>
</td>
<td align="left" width="63%">
Sets the packet values for a particular property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-setpoints">SetPoints</a>
</td>
<td align="left" width="63%">
Sets the points of the stroke using an array of X, Y values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-shear">Shear</a>
</td>
<td align="left" width="63%">
Shears the ink in the stroke by the specified horizontal and vertical factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-split">Split</a>
</td>
<td align="left" width="63%">
Splits the stroke at the specified location on the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-transform">Transform</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_beziercusps">BezierCusps</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_bezierpoints">BezierPoints</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_deleted">Deleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that indicates whether the <b>IInkStrokeDisp</b> object has been deleted from its parent <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_drawingattributes">DrawingAttributes</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties">ExtendedProperties</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id">Id</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_ink">Ink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the parent <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object for this stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetcount">PacketCount</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription">PacketDescription</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetsize">PacketSize</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_polylinecusps">PolylineCusps</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_selfintersections">SelfIntersections</a>


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




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

