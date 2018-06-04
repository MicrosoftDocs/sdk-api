---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D2D1_GEOMETRY_RELATION enumeration


## -description


Describes how one geometry object is spatially related to another geometry object.


## -enum-fields




### -field D2D1_GEOMETRY_RELATION_UNKNOWN

The relationship between the two geometries cannot be determined. This value is never returned by any D2D method.  


### -field D2D1_GEOMETRY_RELATION_DISJOINT

The two geometries  do not intersect at all.


### -field D2D1_GEOMETRY_RELATION_IS_CONTAINED

The instance geometry is entirely contained by  the passed-in geometry.


### -field D2D1_GEOMETRY_RELATION_CONTAINS

The instance geometry entirely contains the passed-in geometry.


### -field D2D1_GEOMETRY_RELATION_OVERLAP

The two geometries overlap but neither completely contains the other. 


### -field D2D1_GEOMETRY_RELATION_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/2b858c8c-6b9b-45bf-8d12-cb14af1987b7">ID2D1Geometry::CompareWithGeometry</a>
 

 

