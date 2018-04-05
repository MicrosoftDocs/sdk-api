---
UID: NE:d3dcommon.D3D_TESSELLATOR_OUTPUT_PRIMITIVE
title: D3D_TESSELLATOR_OUTPUT_PRIMITIVE
author: windows-driver-content
description: Values that identify output primitive types.
old-location: direct3d11\d3d_tessellator_output_primitive.htm
old-project: direct3d11
ms.assetid: 5fdaa41f-0612-4d2e-bb3e-60222f92bc96
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D11_TESSELLATOR_OUTPUT_LINE, D3D11_TESSELLATOR_OUTPUT_POINT, D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW, D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW, D3D11_TESSELLATOR_OUTPUT_UNDEFINED, D3D_TESSELLATOR_OUTPUT_LINE, D3D_TESSELLATOR_OUTPUT_POINT, D3D_TESSELLATOR_OUTPUT_PRIMITIVE, D3D_TESSELLATOR_OUTPUT_PRIMITIVE enumeration [Direct3D 11], D3D_TESSELLATOR_OUTPUT_TRIANGLE_CCW, D3D_TESSELLATOR_OUTPUT_TRIANGLE_CW, D3D_TESSELLATOR_OUTPUT_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_OUTPUT_LINE, d3dcommon/D3D11_TESSELLATOR_OUTPUT_POINT, d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW, d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW, d3dcommon/D3D11_TESSELLATOR_OUTPUT_UNDEFINED, d3dcommon/D3D_TESSELLATOR_OUTPUT_LINE, d3dcommon/D3D_TESSELLATOR_OUTPUT_POINT, d3dcommon/D3D_TESSELLATOR_OUTPUT_PRIMITIVE, d3dcommon/D3D_TESSELLATOR_OUTPUT_TRIANGLE_CCW, d3dcommon/D3D_TESSELLATOR_OUTPUT_TRIANGLE_CW, d3dcommon/D3D_TESSELLATOR_OUTPUT_UNDEFINED, direct3d11.d3d_tessellator_output_primitive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D_TESSELLATOR_OUTPUT_PRIMITIVE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3DCommon.h
api_name:
-	D3D_TESSELLATOR_OUTPUT_PRIMITIVE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

