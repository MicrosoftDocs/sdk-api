---
UID: NE:d2d1.D2D1_GEOMETRY_RELATION
title: D2D1_GEOMETRY_RELATION
author: windows-sdk-content
description: Describes how one geometry object is spatially related to another geometry object.
old-location: direct2d\D2D1_GEOMETRY_RELATION.htm
tech.root: direct2d
ms.assetid: 6c7290c8-9363-414b-af2c-0f2a79da99f9
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D2D1_GEOMETRY_RELATION, D2D1_GEOMETRY_RELATION enumeration [Direct2D], D2D1_GEOMETRY_RELATION_CONTAINS, D2D1_GEOMETRY_RELATION_DISJOINT, D2D1_GEOMETRY_RELATION_IS_CONTAINED, D2D1_GEOMETRY_RELATION_OVERLAP, D2D1_GEOMETRY_RELATION_UNKNOWN, d2d1/D2D1_GEOMETRY_RELATION, d2d1/D2D1_GEOMETRY_RELATION_CONTAINS, d2d1/D2D1_GEOMETRY_RELATION_DISJOINT, d2d1/D2D1_GEOMETRY_RELATION_IS_CONTAINED, d2d1/D2D1_GEOMETRY_RELATION_OVERLAP, d2d1/D2D1_GEOMETRY_RELATION_UNKNOWN, direct2d.D2D1_GEOMETRY_RELATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_GEOMETRY_RELATION
product: Windows
targetos: Windows
req.typenames: D2D1_GEOMETRY_RELATION
req.redist: 
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
 

 

