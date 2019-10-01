---
UID: NN:d2d1.ID2D1GeometryGroup
title: ID2D1GeometryGroup (d2d1.h)
author: windows-sdk-content
description: Represents a composite geometry, composed of other ID2D1Geometry objects.
old-location: direct2d\ID2D1GeometryGroup.htm
tech.root: Direct2D
ms.assetid: 15c3800c-b57c-4c3c-995f-407beee4cc99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1GeometryGroup, ID2D1GeometryGroup interface [Direct2D], ID2D1GeometryGroup interface [Direct2D],described, d2d1/ID2D1GeometryGroup, direct2d.ID2D1GeometryGroup
ms.topic: interface
f1_keywords: 
 - "d2d1/ID2D1GeometryGroup"
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
 - ID2D1GeometryGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GeometryGroup interface


## -description


Represents a composite geometry, composed of other <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GeometryGroup</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>. <b>ID2D1GeometryGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GeometryGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1geometrygroup-getfillmode">GetFillMode</a>
</td>
<td align="left" width="63%">
Indicates how the intersecting areas of the geometries contained in this geometry group are combined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1geometrygroup-getsourcegeometries">GetSourceGeometries</a>
</td>
<td align="left" width="63%">
Retrieves the geometries in the geometry group. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1geometrygroup-getsourcegeometrycount">GetSourceGeometryCount</a>
</td>
<td align="left" width="63%">
Indicates the number of geometry objects in the geometry group. 

</td>
</tr>
</table> 


## -remarks



Geometry groups are a convenient way to group several geometries simultaneously so all figures of several distinct geometries are concatenated into one. 

<h3><a id="Creating_ID2D1GeometryGroup_Objects"></a><a id="creating_id2d1geometrygroup_objects"></a><a id="CREATING_ID2D1GEOMETRYGROUP_OBJECTS"></a>Creating ID2D1GeometryGroup Objects</h3>
To create a  <b>ID2D1GeometryGroup</b> object, call  the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">ID2D1Factory::CreateGeometryGroup</a> method, passing in the <i>fillMode</i> with possible values of   <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE_ALTERNATE</a> (alternate) and <b>D2D1_FILL_MODE_WINDING</b>, an array of geometry objects to add to the geometry group, and the number of elements in this array. 

Direct2D geometries are immutable and device-independent resources created by <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>.


#### Examples

The following code example first declares an array of geometry objects. These objects are four concentric circles that have the following radii: 25, 50, 75, and 100. Then call the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">CreateGeometryGroup</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> object,  passing in <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE_ALTERNATE</a>, an array of geometry objects to add to the geometry group, and the number of elements in this array.  


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




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

