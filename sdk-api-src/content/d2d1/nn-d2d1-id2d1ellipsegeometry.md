---
UID: NN:d2d1.ID2D1EllipseGeometry
title: ID2D1EllipseGeometry
author: windows-sdk-content
description: Represents an ellipse.
old-location: direct2d\ID2D1EllipseGeometry.htm
tech.root: direct2d
ms.assetid: 4ab6452c-6df8-46c0-9e0d-0cebc19d84ba
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1EllipseGeometry, ID2D1EllipseGeometry interface [Direct2D], ID2D1EllipseGeometry interface [Direct2D],described, d2d1/ID2D1EllipseGeometry, direct2d.ID2D1EllipseGeometry
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
 - ID2D1EllipseGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EllipseGeometry interface


## -description


Represents an ellipse.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1EllipseGeometry</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1EllipseGeometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1EllipseGeometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2161bce-b7de-470f-8f3b-130dc2a3c2fc">GetEllipse</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a> structure that describes this ellipse geometry.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1EllipseGeometry_Objects"></a><a id="creating_id2d1ellipsegeometry_objects"></a><a id="CREATING_ID2D1ELLIPSEGEOMETRY_OBJECTS"></a>Creating ID2D1EllipseGeometry Objects</h3>
To create an elipse geometry, use the <a href="https://msdn.microsoft.com/4c03bb0b-74fe-456a-aa26-5449d758c0ea">ID2D1Factory::CreateEllipseGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

