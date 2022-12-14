---
UID: NE:d2d1.D2D1_FILL_MODE
title: D2D1_FILL_MODE (d2d1.h)
description: Specifies how the intersecting areas of geometries or figures are combined to form the area of the composite geometry.
helpviewer_keywords: ["D2D1_FILL_MODE","D2D1_FILL_MODE enumeration [Direct2D]","D2D1_FILL_MODE_ALTERNATE","D2D1_FILL_MODE_WINDING","d2d1/D2D1_FILL_MODE","d2d1/D2D1_FILL_MODE_ALTERNATE","d2d1/D2D1_FILL_MODE_WINDING","direct2d.D2D1_FILL_MODE"]
old-location: direct2d\D2D1_FILL_MODE.htm
tech.root: Direct2D
ms.assetid: f1a14447-39fa-4a48-9516-ff5b03abc3a6
ms.date: 12/05/2018
ms.keywords: D2D1_FILL_MODE, D2D1_FILL_MODE enumeration [Direct2D], D2D1_FILL_MODE_ALTERNATE, D2D1_FILL_MODE_WINDING, d2d1/D2D1_FILL_MODE, d2d1/D2D1_FILL_MODE_ALTERNATE, d2d1/D2D1_FILL_MODE_WINDING, direct2d.D2D1_FILL_MODE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_FILL_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FILL_MODE
 - d2d1/D2D1_FILL_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_FILL_MODE
---

# D2D1_FILL_MODE enumeration


## -description

Specifies how the intersecting areas of geometries or figures are combined to form the area of the composite geometry.

## -enum-fields

### -field D2D1_FILL_MODE_ALTERNATE:0

Determines whether a point is in the fill region by drawing a ray from that point to infinity in any direction, and then counting the number of path segments within the given shape that the ray crosses. If this number is odd, the point is in the fill region; if even, the point is outside the fill region.

### -field D2D1_FILL_MODE_WINDING:1

Determines whether a point is in the fill region of the path by drawing a ray from that point to infinity in any direction, and then examining the places where a segment of the shape crosses the ray. Starting with a count of zero, add one each time a segment crosses the ray from left to right and subtract one each time a path segment crosses the ray from right to left,  as long as left and right are seen from the perspective of the ray. After counting the crossings, if the result is zero, then the point is outside the path. Otherwise, it is inside the path.

### -field D2D1_FILL_MODE_FORCE_DWORD:0xffffffff

## -remarks

Use the <b>D2D1_FILL_MODE</b> enumeration when creating an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a> with the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">CreateGeometryGroup</a> method, or when modifying the fill mode of an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> with the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-setfillmode">ID2D1SimplifiedGeometrySink::SetFillMode</a>  method.

Direct2D fills the interior of a path by using one of the two fill modes specified by this enumeration: <b>D2D1_FILL_MODE_ALTERNATE</b> (alternate) or <b>D2D1_FILL_MODE_WINDING</b> (winding). Because the modes determine how to fill the interior of a closed shape, all shapes are treated as closed when they are filled.  If there is a gap in a segment in a shape, draw an imaginary line to close it. 

 To see the difference between the winding and alternate fill modes, assume that you have four circles with the same center and a different radius, as shown in the following illustration. The first one has the radius of 25, the second 50, the third 75, and the fourth 100.

<img alt="Illustration of four concentric circles with different radius values" src="./images/fillmode_not_filled_01.png"/>
The following  illustration shows the shape filled by using the alternate fill mode. Notice that the center and third ring are not filled. This is because a ray drawn from any point in either of those two rings passes through an even number of segments. 

<img alt="Illustration of concentric circles with the second and fourth rings filled" src="./images/fillmode_01.png"/>
The following illustration explains this process. 

<img alt="Illustration of concentric circles with points in the second and third rings and two arbitrary rays extending from each point" src="./images/fillmode_03.png"/>
The following illustration shows how the same shape is filled when the winding fill mode is specified. 

<img alt="Illustration of concentric circles with all rings filled" src="./images/fillmode_02.png"/>
Notice that all the rings are filled. This is because all the segments run in the same direction, so a ray drawn from any point will cross one or more segments, and the sum of the crossings will not equal zero. 

The following illustration explains this process. The red arrows represent the direction in which the segments are drawn and the black arrow represents an arbitrary ray that runs from a point in the innermost ring. Starting with a value of zero, for each segment that the ray crosses, a value of one is added for every clockwise intersection. All points lie in the fill region in this illustration, because the count does not equal zero. 

<img alt="Illustration of concentric circles with a ray from within the first ring that crosses all four rings" src="./images/fillmode_04.png"/>

## Examples

The following code example creates the geometry groups used the preceding illustrations. The code first declares an array of geometry objects. These objects are four concentric circles that have the following radii: 25, 50, 75, and 100. Then call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">CreateGeometryGroup</a> on the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> object,  passing in <b>D2D1_FILL_MODE_ALTERNATE</b>, an array of geometry objects to add to the geometry group, and the number of elements in this array.  


```cpp
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}

```

## -see-also

<a href="/windows/win32/Direct2D/direct2d-geometries-overview">Geometries Overview</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">ID2D1Factory::CreateGeometryGroup</a>

