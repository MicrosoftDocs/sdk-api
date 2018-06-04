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

# D3D_INTERPOLATION_MODE enumeration


## -description


Specifies interpolation mode, which affects how values are calculated during rasterization.


## -enum-fields




### -field D3D_INTERPOLATION_UNDEFINED

The interpolation mode is undefined.


### -field D3D_INTERPOLATION_CONSTANT

Don't interpolate between register values.


### -field D3D_INTERPOLATION_LINEAR

Interpolate linearly between register values.


### -field D3D_INTERPOLATION_LINEAR_CENTROID

Interpolate linearly between register values but centroid clamped when multisampling.


### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE

Interpolate linearly between register values but with no perspective correction.


### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID

Interpolate linearly between register values but with no perspective correction and centroid clamped when multisampling.


### -field D3D_INTERPOLATION_LINEAR_SAMPLE

Interpolate linearly between register values but sample clamped when multisampling.


### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE

Interpolate linearly between register values but with no perspective correction and sample clamped when multisampling.


## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>



<a href="https://msdn.microsoft.com/C6F1079C-A686-44EA-933B-9DE2D70CFA33">D3D11_PARAMETER_DESC</a>
 

 

