---
UID: NF:d2d1.ID2D1Factory.CreateGeometryGroup
title: ID2D1Factory::CreateGeometryGroup (d2d1.h)
description: Creates an ID2D1GeometryGroup, which is an object that holds other geometries.
helpviewer_keywords: ["CreateGeometryGroup","CreateGeometryGroup method [Direct2D]","CreateGeometryGroup method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateGeometryGroup method","ID2D1Factory.CreateGeometryGroup","ID2D1Factory::CreateGeometryGroup","d2d1/ID2D1Factory::CreateGeometryGroup","direct2d.ID2D1Factory_CreateGeometryGroup"]
old-location: direct2d\ID2D1Factory_CreateGeometryGroup.htm
tech.root: Direct2D
ms.assetid: e69c54b9-eb10-4a7f-8a5b-c42ad4572fa0
ms.date: 12/05/2018
ms.keywords: CreateGeometryGroup, CreateGeometryGroup method [Direct2D], CreateGeometryGroup method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateGeometryGroup method, ID2D1Factory.CreateGeometryGroup, ID2D1Factory::CreateGeometryGroup, d2d1/ID2D1Factory::CreateGeometryGroup, direct2d.ID2D1Factory_CreateGeometryGroup
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory::CreateGeometryGroup
 - d2d1/ID2D1Factory::CreateGeometryGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateGeometryGroup
---

# ID2D1Factory::CreateGeometryGroup


## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a>, which is an object that holds other geometries.

## -parameters

### -param fillMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a></b>

A value that specifies the rule that a composite shape uses to determine whether a given point is part of the geometry.

### -param geometries [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>**</b>

An array containing the geometry objects to add to the geometry group. The number of elements in this array is indicated by the <i>geometriesCount</i> parameter.

### -param geometriesCount

Type: <b>UINT</b>

The number of elements in <i>geometries</i>.

### -param geometryGroup [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a>**</b>

When this method returns, contains the address of a pointer to the geometry group created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Geometry groups are a convenient way to group several geometries simultaneously so all figures of several distinct geometries are concatenated into one. To create a  <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a> object, call  the <b>CreateGeometryGroup</b> method on the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> object, passing in the <i>fillMode</i> with possible values of   <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE_ALTERNATE</a> (alternate) and <b>D2D1_FILL_MODE_WINDING</b>, an array of geometry objects to add to the geometry group, and the number of elements in this array. 


## Examples

The following code example first declares an array of geometry objects. These objects are four concentric circles that have the following radii: 25, 50, 75, and 100. Then call the <b>CreateGeometryGroup</b> on the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> object,  passing in <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE_ALTERNATE</a>, an array of geometry objects to add to the geometry group, and the number of elements in this array.  


```cpp
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

```


The following illustration shows the results of rendering the two group geometries from the example.

<img alt="Illustration of two sets of four concentric circles, one with the second and fourth rings filled and one with all rings filled" src="./images/create_geometry_group.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-geometries-overview">Geometries Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

