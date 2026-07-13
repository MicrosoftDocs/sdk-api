---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentData
title: IXpsOMGeometryFigure::GetSegmentData (xpsobjectmodel.h)
description: Gets the segment data points for the geometry figure.
helpviewer_keywords: ["GetSegmentData","GetSegmentData method [XPS Documents and Packaging]","GetSegmentData method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetSegmentData method","IXpsOMGeometryFigure.GetSegmentData","IXpsOMGeometryFigure::GetSegmentData","xps.ixpsomgeometryfigure_getsegmentdata","xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentData"]
old-location: xps\ixpsomgeometryfigure_getsegmentdata.htm
tech.root: xps
ms.assetid: e2e6be6f-3a9d-4d39-875f-cd23bc82e74b
ms.date: 08/16/2022
ms.keywords: GetSegmentData, GetSegmentData method [XPS Documents and Packaging], GetSegmentData method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentData method, IXpsOMGeometryFigure.GetSegmentData, IXpsOMGeometryFigure::GetSegmentData, xps.ixpsomgeometryfigure_getsegmentdata, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentData
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMGeometryFigure::GetSegmentData
 - xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGeometryFigure.GetSegmentData
---

# IXpsOMGeometryFigure::GetSegmentData


## -description

Gets the segment data points for the geometry figure.

## -parameters

### -param dataCount [in, out]

The size of the array referenced by the <i>segmentData</i> parameter.

If the method returns successfully, <i>dataCount</i> will contain the number of elements returned in the array that is referenced by <i>segmentData</i>.

If <i>segmentData</i> is set to <b>NULL</b> when the method is called,   <i>dataCount</i> must be set to zero.

  If a <b>NULL</b> pointer is returned in <i>segmentData</i>, <i>dataCount</i> will contain the required buffer size as the number of elements.

### -param segmentData [in, out]

The address of an array that has the same number of elements as specified in <i>dataCount</i>. This value can be set to <b>NULL</b> if the caller requires that the method return only the required buffer size in <i>dataCount</i>.

If the array is large enough, this method copies the segment data points into the array and  returns, in <i>dataCount</i>, the number of data points that are copied. If <i>segmentData</i> is set to <b>NULL</b> or references a buffer that is not large enough, a <b>NULL</b> pointer will be returned, no data will be copied, and <i>dataCount</i> will contain the  required buffer size specified as the number of elements.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>dataCount</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>segmentData</i> is <b>NULL</b> or references a buffer that is not large enough to receive the segment data. <i>dataCount</i> contains the required number of elements.

</td>
</tr>
</table>

## -remarks

To determine the required size of the segment data array before calling this method, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdatacount">GetSegmentDataCount</a>. 

A geometry segment is described by the start point, the segment type, and additional parameters whose values are determined by the segment type. The coordinates for the start point of the first segment are a property of the geometry figure and  are set by calling <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setstartpoint">SetStartPoint</a>. The start point of each subsequent segment is the end point of the preceding segment.

The values  in the array returned in the <i>segmentData</i>  parameter will  correspond with the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_type">XPS_SEGMENT_TYPE</a> values  in the array returned by the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmenttypes">GetSegmentTypes</a> method in the <i>segmentTypes</i>  parameter. To read the segment data values correctly, you will need to know the type of each segment in the geometry figure. For example, if the first line segment has a segment type value of <b>XPS_SEGMENT_TYPE_LINE</b>, the first two data values in the <i>segmentData</i> array will be the x and y coordinates of the end point of  that segment; if the next segment has a segment type value of <b>XPS_SEGMENT_TYPE_BEZIER</b>, the next six values in the <i>segmentData</i> array will describe the characteristics of that segment; and so on for each line segment in the geometry figure.

The table that follows describes the specific set of data values that are returned for each segment type. For an example of how to access this data in a program, see the code example that follows.

<table>
<tr>
<th>Segment type</th>
<th>Required data values </th>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_LINE

<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_LINE figure segment" src="./images/segment_type_line.png"/>

</td>
<td>
Two data values:

<dl>
<dd>x-coordinate of the segment line's end point.</dd>
<dd>y-coordinate of the segment line's end point.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE

<img alt="Diagram of an XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE figure segment." src="./images/segment_type_arc_lc.png"/>

</td>
<td>
Five data values:

<dl>
<dd>x-coordinate of the arc's end point.</dd>
<dd>y-coordinate of the arc's end point.</dd>
<dd>Length of the ellipse's radius along the  x-axis.</dd>
<dd>Length of the ellipse's radius along the  y-axis.</dd>
<dd>Rotation angle.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE

<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE figure segment" src="./images/segment_type_arc_sc.png"/>

</td>
<td>
Five data values:

<dl>
<dd>x-coordinate of the arc's end point.</dd>
<dd>y-coordinate of the arc's end point.</dd>
<dd>Length of the ellipse's radius along the  x-axis.</dd>
<dd>Length of the ellipse's radius along the  y-axis.</dd>
<dd>Rotation angle.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE

<img alt="Diagram of an XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE figure segment." src="./images/segment_type_arc_lcc.png"/>

</td>
<td>
Five data values:

<dl>
<dd>x-coordinate of the arc's end point.</dd>
<dd>y-coordinate of the arc's end point.</dd>
<dd>Length of the ellipse's radius along the  x-axis.</dd>
<dd>Length of the ellipse's radius along the  y-axis.</dd>
<dd>Rotation angle.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE

<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE figure segment" src="./images/segment_type_arc_scc.png"/>

</td>
<td>
Five data values:

<dl>
<dd>x-coordinate of the arc's end point.</dd>
<dd>y-coordinate of the arc's end point.</dd>
<dd>Length of the ellipse's radius along the  x-axis.</dd>
<dd>Length of the ellipse's radius along the  y-axis.</dd>
<dd>Rotation angle.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_BEZIER

<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_BEZIER figure segment" src="./images/segment_type_bezier.png"/>

</td>
<td>
Six data values:

<dl>
<dd>x-coordinate of the Bezier curve's first control point.</dd>
<dd>y-coordinate of the Bezier curve's first control point.</dd>
<dd>x-coordinate of the Bezier curve's second control point.</dd>
<dd>y-coordinate of the Bezier curve's second control point.</dd>
<dd>x-coordinate of the Bezier curve's end point.</dd>
<dd>y-coordinate of the Bezier curve's end point.</dd>
</dl>
</td>
</tr>
<tr>
<td>
XPS_SEGMENT_TYPE_QUADRATIC_BEZIER

<img alt="A diagram that shows an example of an XPS_SEGMENT_TYPE_QUADRATIC_BEZIER figure segment" src="./images/segment_type_quad_bezier.png"/>

</td>
<td>
Four data values:

<dl>
<dd>x-coordinate of the Quad Bezier curve's control point.</dd>
<dd>y-coordinate of the Quad Bezier curve's control point.</dd>
<dd>x-coordinate of the Quad Bezier curve's end point.</dd>
<dd>y-coordinate of the Quad Bezier curve's end point.</dd>
</dl>
</td>
</tr>
</table>
 

The following code example accesses the different data points of each segment type  in a geometry figure.


```cpp
    // currentFigure is the pointer to an IXpsOMGeometryFigure
    // that contains the segment data to examine

    HRESULT             hr = S_OK;
    UINT32              numSegments = 0;
    UINT32              numSegmentDataPoints = 0;
    XPS_SEGMENT_TYPE    *segmentTypes = NULL;
    FLOAT               *segmentDataPoints = NULL;
    BOOL                *segmentStrokes = NULL;

    // get number of segments in this figure
    hr = currentFigure->GetSegmentCount (&numSegments);

    if (SUCCEEDED(hr))
    {
        // allocate array for segment data types
        segmentTypes = new (std::nothrow) XPS_SEGMENT_TYPE[numSegments];
        if (segmentTypes == NULL) { hr = E_OUTOFMEMORY; }
    }

    if (SUCCEEDED(hr))
    {
        // allocate array for segment strokes
        segmentStrokes = new (std::nothrow) BOOL[numSegments];
        if (segmentStrokes == NULL) { hr = E_OUTOFMEMORY; }
    }

    if (SUCCEEDED(hr))
    {
        // get array of segment data types
        hr = currentFigure->GetSegmentTypes (&numSegments, segmentTypes);
    }

    if (SUCCEEDED(hr))
    {
        // get size of segment data array
        hr = currentFigure->GetSegmentDataCount (&numSegmentDataPoints);
    }

    if (SUCCEEDED(hr))
    {
        // get array to hold segment data points
        segmentDataPoints = new (std::nothrow) FLOAT[numSegmentDataPoints];
        if (segmentDataPoints == NULL) { hr = E_OUTOFMEMORY; }
    }

    if (SUCCEEDED(hr))
    {
        // get segment data points
        hr = currentFigure->GetSegmentData (
            &numSegmentDataPoints, segmentDataPoints);
    }

    if (SUCCEEDED(hr))
    {
        // process segment data
        UINT32           thisSegment = 0;
        XPS_SEGMENT_TYPE *thisSegmentType = segmentTypes;
        XPS_SEGMENT_TYPE *lastSegmentType = NULL;
        FLOAT            *thisSegmentDataPoint = segmentDataPoints;
        FLOAT            *lastSegmentsDataPoint = NULL;

        // points to element just after valid array
        // valid pointers are < this value and  >= &segmentTypes[0]
        lastSegmentType = &segmentTypes[numSegments]; 
        // points to element just after valid array
        // valid pointers are < this value and >= &segmentDataPoints[0]
        lastSegmentsDataPoint = &segmentDataPoints[numSegmentDataPoints];

        // look at each segment that was returned
        while (thisSegment < numSegments)
        {
            if ((thisSegmentType >= lastSegmentType) || 
                (thisSegmentDataPoint >= lastSegmentsDataPoint))
            {
                // the array data is not correct.
                hr = E_UNEXPECTED;
                break; // out of loop
            } 
            else
            {
                // process the data based on the segment type
                switch (*thisSegmentType) 
                {
                    case    XPS_SEGMENT_TYPE_ARC_LARGE_CLOCKWISE:
                    case    XPS_SEGMENT_TYPE_ARC_LARGE_COUNTERCLOCKWISE:
                    case    XPS_SEGMENT_TYPE_ARC_SMALL_CLOCKWISE:
                    case    XPS_SEGMENT_TYPE_ARC_SMALL_COUNTERCLOCKWISE:
                        {
                        // 5 data points
                        FLOAT    arcEndPoint_x = *thisSegmentDataPoint++;
                        FLOAT    arcEndPoint_y = *thisSegmentDataPoint++;
                        FLOAT    radius_x = *thisSegmentDataPoint++;
                        FLOAT    radius_y = *thisSegmentDataPoint++;
                        FLOAT    angle = *thisSegmentDataPoint++;
                        // do something with these points
                        }
                        break;
                    case    XPS_SEGMENT_TYPE_BEZIER:
                        {
                        // 6 data points
                        FLOAT    controlPoint1_x = *thisSegmentDataPoint++;
                        FLOAT    controlPoint1_y = *thisSegmentDataPoint++;
                        FLOAT    controlPoint2_x = *thisSegmentDataPoint++;
                        FLOAT    controlPoint2_y = *thisSegmentDataPoint++;
                        FLOAT    endPoint_x = *thisSegmentDataPoint++;
                        FLOAT    endPoint_y = *thisSegmentDataPoint++;
                        // do something with these points
                        }
                        break;
                    case    XPS_SEGMENT_TYPE_LINE:
                        {
                        // 2 data points
                        FLOAT    endPoint_x = *thisSegmentDataPoint++;
                        FLOAT    endPoint_y = *thisSegmentDataPoint++;
                        // do something with these points
                        }
                        break;
                    case    XPS_SEGMENT_TYPE_QUADRATIC_BEZIER:
                        {
                        // 4 data points
                        FLOAT    controlPoint_x = *thisSegmentDataPoint++;
                        FLOAT    controlPoint_y = *thisSegmentDataPoint++;
                        FLOAT    endPoint_x = *thisSegmentDataPoint++;
                        FLOAT    endPoint_y = *thisSegmentDataPoint++;
                        // do something with these points
                        }
                        break;
                    default:
                        // unrecognized segment type
                        break;
                }
                // 
                thisSegment++;
                thisSegmentType++;
            }
        }
    }

    delete[] segmentTypes; segmentTypes = NULL;
    delete[] segmentStrokes; segmentStrokes = NULL;
    delete[] segmentDataPoints; segmentDataPoints = NULL;

```

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentcount">GetSegmentCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdatacount">GetSegmentDataCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmenttypes">GetSegmentTypes</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>