---
UID: NN:d2d1.ID2D1RoundedRectangleGeometry
title: ID2D1RoundedRectangleGeometry
author: windows-sdk-content
description: Describes a rounded rectangle.
old-location: direct2d\ID2D1RoundedRectangleGeometry.htm
tech.root: direct2d
ms.assetid: e49e9be7-155a-4487-9931-035f18771c04
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1RoundedRectangleGeometry, ID2D1RoundedRectangleGeometry interface [Direct2D], ID2D1RoundedRectangleGeometry interface [Direct2D],described, d2d1/ID2D1RoundedRectangleGeometry, direct2d.ID2D1RoundedRectangleGeometry
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
 - ID2D1RoundedRectangleGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RoundedRectangleGeometry interface


## -description


Describes a rounded rectangle.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RoundedRectangleGeometry</b> interface inherits from <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>. <b>ID2D1RoundedRectangleGeometry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1RoundedRectangleGeometry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f9abc57-bb0b-4e90-8478-eef05456f9d8">GetRoundedRect</a>
</td>
<td align="left" width="63%">
Retrieves a rounded rectangle that describes this rounded rectangle geometry.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1RoundedRectangleGeometry_Objects"></a><a id="creating_id2d1roundedrectanglegeometry_objects"></a><a id="CREATING_ID2D1ROUNDEDRECTANGLEGEOMETRY_OBJECTS"></a>Creating ID2D1RoundedRectangleGeometry Objects</h3>
To create a rectangle geometry, use the <a href="https://msdn.microsoft.com/b0f7ccb0-5733-4f96-a532-8f665fbc257e">ID2D1Factory::CreateRoundedRectangleGeometry</a> method.

Direct2D geometries are immutable and device-independent resources created by <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>.  In general, you should create geometries once and retain them for the life of the application, or until they need to be modified. For more information about device-independent and device-dependent resources, see  the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>. 




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

