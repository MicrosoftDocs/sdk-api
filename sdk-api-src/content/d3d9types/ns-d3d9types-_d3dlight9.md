---
UID: NS:d3d9types._D3DLIGHT9
title: "_D3DLIGHT9"
author: windows-driver-content
description: Defines a set of lighting properties.
old-location: direct3d9\d3dlight9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dlight9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DLIGHT9, D3DLIGHT9 structure [Direct3D 9], LPD3DLIGHT, LPD3DLIGHT structure pointer [Direct3D 9], _D3DLIGHT9, a7c738d5-682c-9821-12b7-bd62698a702c, d3d9types/D3DLIGHT9, d3d9types/LPD3DLIGHT, direct3d9.d3dlight9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DLIGHT9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DLIGHT9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DLIGHT9 structure


## -description


Defines a set of lighting properties.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/90ad82d3-ffa8-42bb-9d9c-cf28a416c32d">D3DLIGHTTYPE</a></b>

Type of the light source. This value is one of the members of the <a href="https://msdn.microsoft.com/90ad82d3-ffa8-42bb-9d9c-cf28a416c32d">D3DLIGHTTYPE</a> enumerated type. 


### -field Diffuse

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Diffuse color emitted by the light. This member is a <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a> structure. 


### -field Specular

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Specular color emitted by the light. This member is a <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a> structure. 


### -field Ambient

Type: <b><a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a></b>

Ambient color emitted by the light. This member is a <a href="https://msdn.microsoft.com/6af8c2ec-bc79-4dc6-b56d-7a7676a50b39">D3DCOLORVALUE</a> structure. 


### -field Position

Type: <b><a href="https://msdn.microsoft.com/7091617b-935b-466e-8270-90240a1adaee">D3DVECTOR</a></b>

Position of the light in world space, specified by a <a href="https://msdn.microsoft.com/7091617b-935b-466e-8270-90240a1adaee">D3DVECTOR</a> structure. This member has no meaning for directional lights and is ignored in that case. 


### -field Direction

Type: <b><a href="https://msdn.microsoft.com/7091617b-935b-466e-8270-90240a1adaee">D3DVECTOR</a></b>

Direction that the light is pointing in world space, specified by a <a href="https://msdn.microsoft.com/7091617b-935b-466e-8270-90240a1adaee">D3DVECTOR</a> structure. This member has meaning only for directional and spotlights. This vector need not be normalized, but it should have a nonzero length. 


### -field Range

Type: <b>float</b>

Distance beyond which the light has no effect. The maximum allowable value for this member is the square root of FLT_MAX. This member does not affect directional lights. 


### -field Falloff

Type: <b>float</b>

Decrease in illumination between a spotlight's inner cone (the angle specified by 
    Theta) and the outer edge of the outer cone (the angle specified by Phi). 

The effect of falloff on the lighting is subtle. Furthermore, a small performance penalty is incurred by shaping the falloff curve. For these reasons, most developers set this value to 1.0.


### -field Attenuation0

Type: <b>float</b>

Value specifying how the light intensity changes over distance. Attenuation values are ignored for directional lights. This member represents an attenuation constant. For information about attenuation, see <a href="https://msdn.microsoft.com/b39f1287-c67b-4cbb-b599-4a1b2f4981ac">Light Properties (Direct3D 9)</a>. Valid values for this member range from 0.0 to infinity. For non-directional lights, all three attenuation values should not be set to 0.0 at the same time. 


### -field Attenuation1

Type: <b>float</b>

Value specifying how the light intensity changes over distance. Attenuation values are ignored for directional lights. This member represents an attenuation constant. For information about attenuation, see <a href="https://msdn.microsoft.com/b39f1287-c67b-4cbb-b599-4a1b2f4981ac">Light Properties (Direct3D 9)</a>. Valid values for this member range from 0.0 to infinity. For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.


### -field Attenuation2

Type: <b>float</b>

Value specifying how the light intensity changes over distance. Attenuation values are ignored for directional lights. This member represents an attenuation constant. For information about attenuation, see <a href="https://msdn.microsoft.com/b39f1287-c67b-4cbb-b599-4a1b2f4981ac">Light Properties (Direct3D 9)</a>. Valid values for this member range from 0.0 to infinity. For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.


### -field Theta

Type: <b>float</b>

Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone. This value must be in the range from 0 through the value specified by Phi.


### -field Phi

Type: <b>float</b>

Angle, in radians, defining the outer edge of the spotlight's outer cone. Points outside this cone are not lit by the spotlight. This value must be between 0 and pi. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/1e52be8e-7e24-400d-89c5-93dd316534bc">GetLight</a>



<a href="https://msdn.microsoft.com/e1f07ba6-8a9f-4bac-8dad-16160559fa4c">SetLight</a>
 

 

