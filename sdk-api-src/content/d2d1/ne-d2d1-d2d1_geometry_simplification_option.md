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

# D2D1_GEOMETRY_SIMPLIFICATION_OPTION enumeration


## -description


Specifies how a geometry is simplified to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>.


## -enum-fields




### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_CUBICS_AND_LINES

The output can contain cubic Bezier curves and line segments.


### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES

The output is flattened so that it contains only line segments. 


### -field D2D1_GEOMETRY_SIMPLIFICATION_OPTION_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/49f73c2d-9f86-482f-8289-fef28a461e01">ID2D1Geometry::Simplify</a>
 

 

