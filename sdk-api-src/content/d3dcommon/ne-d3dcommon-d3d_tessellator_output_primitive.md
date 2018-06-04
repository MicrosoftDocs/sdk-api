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

# D3D_TESSELLATOR_OUTPUT_PRIMITIVE enumeration


## -description


Values that identify output primitive types.


## -enum-fields




### -field D3D_TESSELLATOR_OUTPUT_UNDEFINED

The output primitive type is undefined.


### -field D3D_TESSELLATOR_OUTPUT_POINT

The output primitive type is a point.


### -field D3D_TESSELLATOR_OUTPUT_LINE

The output primitive type is a line.


### -field D3D_TESSELLATOR_OUTPUT_TRIANGLE_CW

The output primitive type is a clockwise triangle.


### -field D3D_TESSELLATOR_OUTPUT_TRIANGLE_CCW

The output primitive type is a counter clockwise triangle.


### -field D3D11_TESSELLATOR_OUTPUT_UNDEFINED

The output primitive type is undefined.


### -field D3D11_TESSELLATOR_OUTPUT_POINT

The output primitive type is a point.


### -field D3D11_TESSELLATOR_OUTPUT_LINE

The output primitive type is a line.


### -field D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW

The output primitive type is a clockwise triangle.


### -field D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW

The output primitive type is a counter clockwise triangle.


## -remarks



The output primitive type determines how the tessellator output data is organized; this enumeration is used by <a href="https://msdn.microsoft.com/25c8f773-e319-4ba1-b332-d45b8323e8c8">D3D11_SHADER_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

