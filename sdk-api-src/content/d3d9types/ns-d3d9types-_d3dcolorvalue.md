---
UID: NS:d3d9types._D3DCOLORVALUE
title: "_D3DCOLORVALUE"
author: windows-driver-content
description: Describes color values.
old-location: direct3d9\d3dcolorvalue.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcolorvalue.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 5e92d054-aea6-ea14-1f84-776bc919203e, D3DCOLORVALUE, D3DCOLORVALUE structure [Direct3D 9], _D3DCOLORVALUE, d3d9types/D3DCOLORVALUE, direct3d9.d3dcolorvalue
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
req.typenames: D3DCOLORVALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DCOLORVALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCOLORVALUE structure


## -description


Describes color values.


## -struct-fields




### -field r

Type: <b>float</b>

Floating-point value that specifies the red component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.


### -field g

Type: <b>float</b>

Floating-point value that specifies the green component of a color. This value generally is in the range from 0.0 through 1.0.  A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.


### -field b

Type: <b>float</b>

Floating-point value that specifies the blue component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.


### -field a

Type: <b>float</b>

Floating-point value that specifies the alpha component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.


## -remarks



You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects. Values greater than 1 produce strong lights that tend to wash out a scene. Negative values produce dark lights that actually remove light from a scene. 




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

