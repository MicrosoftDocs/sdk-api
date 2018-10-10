---
UID: NF:d2d1.ID2D1GeometryGroup.GetSourceGeometries
title: ID2D1GeometryGroup::GetSourceGeometries
author: windows-sdk-content
description: Retrieves the geometries in the geometry group.
old-location: direct2d\ID2D1GeometryGroup_GetSourceGeometries.htm
tech.root: Direct2D
ms.assetid: 11c375a1-aea0-44bf-abcb-ee071140525a
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetSourceGeometries, GetSourceGeometries method [Direct2D], GetSourceGeometries method [Direct2D],ID2D1GeometryGroup interface, ID2D1GeometryGroup interface [Direct2D],GetSourceGeometries method, ID2D1GeometryGroup.GetSourceGeometries, ID2D1GeometryGroup::GetSourceGeometries, d2d1/ID2D1GeometryGroup::GetSourceGeometries, direct2d.ID2D1GeometryGroup_GetSourceGeometries
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
 - ID2D1GeometryGroup.GetSourceGeometries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GeometryGroup::GetSourceGeometries


## -description


Retrieves the geometries in the geometry group. 


## -parameters




### -param geometries [out]

Type: <b>const <a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>**</b>

When this method returns, contains the address of a pointer to an array of geometries to be filled by this method. The length of the array is specified by the <i>geometryCount</i> parameter. If the array is <b>NULL</b>, then this method performs no operation. You must allocate the memory for this array.


### -param geometriesCount

Type: <b>UINT</b>

A value indicating the number of geometries to return in the <i>geometries</i> array. If this value is less than the number of geometries in the geometry group, the remaining geometries are omitted. If this value is larger than the number of geometries in the geometry group, the extra geometries are set to <b>NULL</b>. To obtain the number of geometries currently in the geometry group, use the <a href="https://msdn.microsoft.com/d5338e38-98b7-4e17-933c-f806bd030f88">GetSourceGeometryCount</a> method.


## -returns



This method does not return a value.




## -remarks



The returned geometries are referenced and  counted, and the caller must release them.




## -see-also




<a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a>
 

 

