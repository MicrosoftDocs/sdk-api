---
UID: NN:d2d1.ID2D1GeometryGroup
title: ID2D1GeometryGroup
author: windows-sdk-content
description: Represents a composite geometry, composed of other ID2D1Geometry objects.
old-location: direct2d\ID2D1GeometryGroup.htm
tech.root: direct2d
ms.assetid: 15c3800c-b57c-4c3c-995f-407beee4cc99
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID2D1GeometryGroup, ID2D1GeometryGroup interface [Direct2D], ID2D1GeometryGroup interface [Direct2D],described, d2d1/ID2D1GeometryGroup, direct2d.ID2D1GeometryGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GeometryGroup interface


## -description


Represents a composite geometry, composed of other <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GeometryGroup</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1GeometryGroup</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e248d28e-861b-49b9-a3f7-789604f8eedf">GetFillMode</a>
</td>
<td align="left" width="63%">
Indicates how the intersecting areas of the geometries contained in this geometry group are combined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11c375a1-aea0-44bf-abcb-ee071140525a">GetSourceGeometries</a>
</td>
<td align="left" width="63%">
Retrieves the geometries in the geometry group. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5338e38-98b7-4e17-933c-f806bd030f88">GetSourceGeometryCount</a>
</td>
<td align="left" width="63%">
Indicates the number of geometry objects in the geometry group. 

</td>
</tr>
</table> 


## -remarks



Geometry groups are a convenient way to group several geometries simultaneously so all figures of several distinct geometries are concatenated into one. 

<h3><a id="Creating_ID2D1GeometryGroup_Objects"></a><a id="creating_id2d1geometrygroup_objects"></a><a id="CREATING_ID2D1GEOMETRYGROUP_OBJECTS"></a>Creating ID2D1GeometryGroup Objects</h3>
To create a  <b>ID2D1GeometryGroup</b> object, call  the <a href="https://msdn.microsoft.com/e69c54b9-eb10-4a7f-8a5b-c42ad4572fa0">ID2D1Factory::CreateGeometryGroup</a> method, passing in the <i>fillMode</i> with possible values of   <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE_ALTERNATE</a> (alternate) and <b>D2D1_FILL_MODE_WINDING</b>, an array of geometry objects to add to the geometry group, and the number of elements in this array. 

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.


#### Examples

The following code example first declares an array of geometry objects. These objects are four concentric circles that have the following radii: 25, 50, 75, and 100. Then call the <a href="https://msdn.microsoft.com/e69c54b9-eb10-4a7f-8a5b-c42ad4572fa0">CreateGeometryGroup</a> on the <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> object,  passing in <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE_ALTERNATE</a>, an array of geometry objects to add to the geometry group, and the number of elements in this array.  

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory-&gt;CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &amp;m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory-&gt;CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &amp;m_pGeoGroup_WindingFill
        );
}
</pre>
</td>
</tr>
</table></span></div>
The following illustration shows the results of rendering the two group geometries from the example.

<img alt="Illustration of two sets of four concentric circles, one with the second and fourth rings filled and one with all rings filled" src="images/create_geometry_group.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

