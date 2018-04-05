---
UID: NE:d3d9types._D3DTEXTURESTAGESTATETYPE
title: "_D3DTEXTURESTAGESTATETYPE"
author: windows-driver-content
description: Texture stage states define multi-blender texture operations.
old-location: direct3d9\D3DTEXTURESTAGESTATETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtexturestagestatetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 8dec56ed-b0fb-5918-035f-881fe2e6ee6d, D3DTEXTURESTAGESTATETYPE, D3DTEXTURESTAGESTATETYPE enumeration [Direct3D 9], D3DTSS_ALPHAARG0, D3DTSS_ALPHAARG1, D3DTSS_ALPHAARG2, D3DTSS_ALPHAOP, D3DTSS_BUMPENVLOFFSET, D3DTSS_BUMPENVLSCALE, D3DTSS_BUMPENVMAT00, D3DTSS_BUMPENVMAT01, D3DTSS_BUMPENVMAT10, D3DTSS_BUMPENVMAT11, D3DTSS_COLORARG0, D3DTSS_COLORARG1, D3DTSS_COLORARG2, D3DTSS_COLOROP, D3DTSS_CONSTANT, D3DTSS_FORCE_DWORD, D3DTSS_RESULTARG, D3DTSS_TEXCOORDINDEX, D3DTSS_TEXTURETRANSFORMFLAGS, LPD3DTEXTURESTAGESTATETYPE, LPD3DTEXTURESTAGESTATETYPE enumeration pointer [Direct3D 9], _D3DTEXTURESTAGESTATETYPE, d3d9types/D3DTEXTURESTAGESTATETYPE, d3d9types/D3DTSS_ALPHAARG0, d3d9types/D3DTSS_ALPHAARG1, d3d9types/D3DTSS_ALPHAARG2, d3d9types/D3DTSS_ALPHAOP, d3d9types/D3DTSS_BUMPENVLOFFSET, d3d9types/D3DTSS_BUMPENVLSCALE, d3d9types/D3DTSS_BUMPENVMAT00, d3d9types/D3DTSS_BUMPENVMAT01, d3d9types/D3DTSS_BUMPENVMAT10, d3d9types/D3DTSS_BUMPENVMAT11, d3d9types/D3DTSS_COLORARG0, d3d9types/D3DTSS_COLORARG1, d3d9types/D3DTSS_COLORARG2, d3d9types/D3DTSS_COLOROP, d3d9types/D3DTSS_CONSTANT, d3d9types/D3DTSS_FORCE_DWORD, d3d9types/D3DTSS_RESULTARG, d3d9types/D3DTSS_TEXCOORDINDEX, d3d9types/D3DTSS_TEXTURETRANSFORMFLAGS, d3d9types/LPD3DTEXTURESTAGESTATETYPE, direct3d9.D3DTEXTURESTAGESTATETYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3DTEXTURESTAGESTATETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTEXTURESTAGESTATETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTEXTURESTAGESTATETYPE enumeration


## -description


Texture stage states define multi-blender texture operations. Some sampler states set up vertex processing, and some set up pixel processing. Texture stage states can be saved and restored using stateblocks (see <a href="https://msdn.microsoft.com/6b1917a8-8685-40c3-983d-6bd2fed95642">State Blocks Save and Restore State (Direct3D 9)</a>).


## -enum-fields




### -field D3DTSS_COLOROP

Texture-stage state is a texture color blending operation identified by one member of the <a href="https://msdn.microsoft.com/7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3">D3DTEXTUREOP</a> enumerated type. The default value for the first texture stage (stage 0) is D3DTOP_MODULATE; for all other stages the default is D3DTOP_DISABLE. 


### -field D3DTSS_COLORARG1

Texture-stage state is the first color argument for the stage, identified by one of the <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. The default argument is D3DTA_TEXTURE. 

Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default value for the register is (0.0, 0.0, 0.0, 0.0).


### -field D3DTSS_COLORARG2

Texture-stage state is the second color argument for the stage, identified by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. The default argument is D3DTA_CURRENT. Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default value for the register is (0.0, 0.0, 0.0, 0.0)


### -field D3DTSS_ALPHAOP

Texture-stage state is a texture alpha blending operation identified by one member of the <a href="https://msdn.microsoft.com/7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3">D3DTEXTUREOP</a> enumerated type. The default value for the first texture stage (stage 0) is D3DTOP_SELECTARG1, and for all other stages the default is D3DTOP_DISABLE. 


### -field D3DTSS_ALPHAARG1

Texture-stage state is the first alpha argument for the stage, identified by by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. The default argument is D3DTA_TEXTURE. If no texture is set for this stage, the default argument is D3DTA_DIFFUSE. Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default value for the register is (0.0, 0.0, 0.0, 0.0).


### -field D3DTSS_ALPHAARG2

Texture-stage state is the second alpha argument for the stage, identified by by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. The default argument is D3DTA_CURRENT. Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default value for the register is (0.0, 0.0, 0.0, 0.0). 


### -field D3DTSS_BUMPENVMAT00

Texture-stage state is a floating-point value for the [0][0] coefficient in a bump-mapping matrix. The default value is 0.0. 


### -field D3DTSS_BUMPENVMAT01

Texture-stage state is a floating-point value for the [0][1] coefficient in a bump-mapping matrix. The default value is 0.0. 


### -field D3DTSS_BUMPENVMAT10

Texture-stage state is a floating-point value for the [1][0] coefficient in a bump-mapping matrix. The default value is 0.0. 


### -field D3DTSS_BUMPENVMAT11

Texture-stage state is a floating-point value for the [1][1] coefficient in a bump-mapping matrix. The default value is 0.0. 


### -field D3DTSS_TEXCOORDINDEX

Index of the texture coordinate set to use with this texture stage. You can specify up to eight sets of texture coordinates per vertex. If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).

When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value. The default index for each stage is equal to the stage index. Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.

Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation. For a list of all the constants, see <a href="https://msdn.microsoft.com/b15509b4-7db1-429a-9468-be7a11dee505">D3DTSS_TCI</a>.

With the exception of D3DTSS_TCI_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode. These flags are most useful when performing environment mapping.


### -field D3DTSS_BUMPENVLSCALE

Floating-point scale value for bump-map luminance. The default value is 0.0. 


### -field D3DTSS_BUMPENVLOFFSET

Floating-point offset value for bump-map luminance. The default value is 0.0. 


### -field D3DTSS_TEXTURETRANSFORMFLAGS

Member of the <a href="https://msdn.microsoft.com/a91f33ce-2db5-437a-ac29-402b26b0d4e1">D3DTEXTURETRANSFORMFLAGS</a> enumerated type that controls the transformation of texture coordinates for this texture stage. The default value is D3DTTFF_DISABLE. 


### -field D3DTSS_COLORARG0

Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. This setting is supported if the D3DTEXOPCAPS_MULTIPLYADD or D3DTEXOPCAPS_LERP device capabilities are present. The default argument is D3DTA_CURRENT. Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default value for the register is (0.0, 0.0, 0.0, 0.0). 


### -field D3DTSS_ALPHAARG0

Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. This setting is supported if the D3DTEXOPCAPS_MULTIPLYADD or D3DTEXOPCAPS_LERP device capabilities are present. The default argument is D3DTA_CURRENT. Specify D3DTA_TEMP to select a temporary register color for read or write. D3DTA_TEMP is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. The default argument is (0.0, 0.0, 0.0, 0.0). 


### -field D3DTSS_RESULTARG

Setting to select destination register for the result of this stage, identified by <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>. This value can be set to D3DTA_CURRENT (the default value) or to D3DTA_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument. The final color passed to the fog blender and frame buffer is taken from D3DTA_CURRENT, so the last active texture stage state must be set to write to current. This setting is supported if the D3DPMISCCAPS_TSSARGTEMP device capability is present. 


### -field D3DTSS_CONSTANT

Per-stage constant color. To see if a device supports a per-stage constant color, see the D3DPMISCCAPS_PERSTAGECONSTANT constant in <a href="https://msdn.microsoft.com/7912c682-c179-453b-8a34-e87958217500">D3DPMISCCAPS</a>. D3DTSS_CONSTANT is used by D3DTA_CONSTANT. See <a href="https://msdn.microsoft.com/36b2b715-5ced-4246-840e-8ea343521ef4">D3DTA</a>.  


### -field D3DTSS_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Members of this enumerated type are used with the <a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">IDirect3DDevice9::GetTextureStageState</a> and <a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a> methods to retrieve and set texture state values.

The valid range of values for the D3DTSS_BUMPENVMAT00, D3DTSS_BUMPENVMAT01, D3DTSS_BUMPENVMAT10, and D3DTSS_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0. This range, expressed in mathematical notation is (-8.0,8.0).




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>
 

 

