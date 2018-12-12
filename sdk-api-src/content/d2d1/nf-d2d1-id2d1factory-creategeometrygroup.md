---
UID: NF:d2d1.ID2D1Factory.CreateGeometryGroup
title: ID2D1Factory::CreateGeometryGroup
author: windows-sdk-content
description: Creates an ID2D1GeometryGroup, which is an object that holds other geometries.
old-location: direct2d\ID2D1Factory_CreateGeometryGroup.htm
tech.root: direct2d
ms.assetid: e69c54b9-eb10-4a7f-8a5b-c42ad4572fa0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateGeometryGroup, CreateGeometryGroup method [Direct2D], CreateGeometryGroup method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateGeometryGroup method, ID2D1Factory.CreateGeometryGroup, ID2D1Factory::CreateGeometryGroup, d2d1/ID2D1Factory::CreateGeometryGroup, direct2d.ID2D1Factory_CreateGeometryGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateGeometryGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateGeometryGroup


## -description


Creates an <a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a>, which is an object that holds other geometries.


## -parameters




### -param fillMode

Type: <b><a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE</a></b>

A value that specifies the rule that a composite shape uses to determine whether a given point is part of the geometry. 


### -param geometries [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>**</b>

An array containing the geometry objects to add to the geometry group. The number of elements in this array is indicated by the <i>geometriesCount</i> parameter.


### -param geometriesCount

Type: <b>UINT</b>

The number of elements in <i>geometries</i>.


### -param geometryGroup [out]

Type: <b><a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a>**</b>

When this method returns, contains the address of a pointer to the geometry group created by this method.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Geometry groups are a convenient way to group several geometries simultaneously so all figures of several distinct geometries are concatenated into one. To create a  <a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a> object, call  the <b>CreateGeometryGroup</b> method on the <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> object, passing in the <i>fillMode</i> with possible values of   <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE_ALTERNATE</a> (alternate) and <b>D2D1_FILL_MODE_WINDING</b>, an array of geometry objects to add to the geometry group, and the number of elements in this array. 


#### Examples

The following code example first declares an array of geometry objects. These objects are four concentric circles that have the following radii: 25, 50, 75, and 100. Then call the <b>CreateGeometryGroup</b> on the <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> object,  passing in <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE_ALTERNATE</a>, an array of geometry objects to add to the geometry group, and the number of elements in this array.  


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




<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

