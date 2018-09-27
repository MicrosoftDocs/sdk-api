---
UID: NN:d2d1.ID2D1RectangleGeometry
title: ID2D1RectangleGeometry
author: windows-sdk-content
description: Describes a two-dimensional rectangle.
old-location: direct2d\ID2D1RectangleGeometry.htm
tech.root: direct2d
ms.assetid: bb5f65ba-34d4-418b-863c-2431046bce8e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID2D1RectangleGeometry, ID2D1RectangleGeometry interface [Direct2D], ID2D1RectangleGeometry interface [Direct2D],described, d2d1/ID2D1RectangleGeometry, direct2d.ID2D1RectangleGeometry
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
 - ID2D1RectangleGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RectangleGeometry interface


## -description


Describes a two-dimensional rectangle. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RectangleGeometry</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1RectangleGeometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1RectangleGeometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c9858d0-abb0-4ab5-8e7f-e613b256bbd7">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle that describes the rectangle geometry's dimensions.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1RectangleGeometry_Objects"></a><a id="creating_id2d1rectanglegeometry_objects"></a><a id="CREATING_ID2D1RECTANGLEGEOMETRY_OBJECTS"></a>Creating ID2D1RectangleGeometry Objects</h3>
To create a rectangle geometry, use the <a href="https://msdn.microsoft.com/4c8f4950-7b5a-4f77-9a5b-513916f83d0c">ID2D1Factory::CreateRectangleGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>. 




## -see-also




<a href="https://msdn.microsoft.com/f5870d4b-dd30-4034-884e-1c398a6865c6">Geometries Overview</a>



<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

