---
UID: NE:d3d9types._D3DTEXTUREOP
title: "_D3DTEXTUREOP"
author: windows-driver-content
description: Defines per-stage texture-blending operations.
old-location: direct3d9\D3DTEXTUREOP.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtextureop.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 31f1f21a-7633-d75f-cea7-661f3b3827d6, D3DTEXTUREOP, D3DTEXTUREOP enumeration [Direct3D 9], D3DTOP_ADD, D3DTOP_ADDSIGNED, D3DTOP_ADDSIGNED2X, D3DTOP_ADDSMOOTH, D3DTOP_BLENDCURRENTALPHA, D3DTOP_BLENDDIFFUSEALPHA, D3DTOP_BLENDFACTORALPHA, D3DTOP_BLENDTEXTUREALPHA, D3DTOP_BLENDTEXTUREALPHAPM, D3DTOP_BUMPENVMAP, D3DTOP_BUMPENVMAPLUMINANCE, D3DTOP_DISABLE, D3DTOP_DOTPRODUCT3, D3DTOP_FORCE_DWORD, D3DTOP_LERP, D3DTOP_MODULATE, D3DTOP_MODULATE2X, D3DTOP_MODULATE4X, D3DTOP_MODULATEALPHA_ADDCOLOR, D3DTOP_MODULATECOLOR_ADDALPHA, D3DTOP_MODULATEINVALPHA_ADDCOLOR, D3DTOP_MODULATEINVCOLOR_ADDALPHA, D3DTOP_MULTIPLYADD, D3DTOP_PREMODULATE, D3DTOP_SELECTARG1, D3DTOP_SELECTARG2, D3DTOP_SUBTRACT, LPD3DTEXTUREOP, LPD3DTEXTUREOP enumeration pointer [Direct3D 9], _D3DTEXTUREOP, d3d9types/D3DTEXTUREOP, d3d9types/D3DTOP_ADD, d3d9types/D3DTOP_ADDSIGNED, d3d9types/D3DTOP_ADDSIGNED2X, d3d9types/D3DTOP_ADDSMOOTH, d3d9types/D3DTOP_BLENDCURRENTALPHA, d3d9types/D3DTOP_BLENDDIFFUSEALPHA, d3d9types/D3DTOP_BLENDFACTORALPHA, d3d9types/D3DTOP_BLENDTEXTUREALPHA, d3d9types/D3DTOP_BLENDTEXTUREALPHAPM, d3d9types/D3DTOP_BUMPENVMAP, d3d9types/D3DTOP_BUMPENVMAPLUMINANCE, d3d9types/D3DTOP_DISABLE, d3d9types/D3DTOP_DOTPRODUCT3, d3d9types/D3DTOP_FORCE_DWORD, d3d9types/D3DTOP_LERP, d3d9types/D3DTOP_MODULATE, d3d9types/D3DTOP_MODULATE2X, d3d9types/D3DTOP_MODULATE4X, d3d9types/D3DTOP_MODULATEALPHA_ADDCOLOR, d3d9types/D3DTOP_MODULATECOLOR_ADDALPHA, d3d9types/D3DTOP_MODULATEINVALPHA_ADDCOLOR, d3d9types/D3DTOP_MODULATEINVCOLOR_ADDALPHA, d3d9types/D3DTOP_MULTIPLYADD, d3d9types/D3DTOP_PREMODULATE, d3d9types/D3DTOP_SELECTARG1, d3d9types/D3DTOP_SELECTARG2, d3d9types/D3DTOP_SUBTRACT, d3d9types/LPD3DTEXTUREOP, direct3d9.D3DTEXTUREOP
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
req.typenames: D3DTEXTUREOP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTEXTUREOP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTEXTUREOP enumeration


## -description


Defines per-stage texture-blending operations.


## -enum-fields




### -field D3DTOP_DISABLE

Disables output from this texture stage and all stages with a higher index. To disable texture mapping, set this as the color operation for the first texture stage (stage 0). Alpha operations cannot be disabled when color operations are enabled. Setting the alpha operation to D3DTOP_DISABLE when color blending is enabled causes undefined behavior. 


### -field D3DTOP_SELECTARG1

Use this texture stage's first color or alpha argument, unmodified, as the output. This operation affects the color argument when used with the D3DTSS_COLOROP texture-stage state, and the alpha argument when used with D3DTSS_ALPHAOP. 

<img alt="Equation of this argument (S(RGBA) = Arg1)" src="images/topfrm1.png"/>


### -field D3DTOP_SELECTARG2

Use this texture stage's second color or alpha argument, unmodified, as the output. This operation affects the color argument when used with the D3DTSS_COLOROP texture stage state, and the alpha argument when used with D3DTSS_ALPHAOP. 

<img alt="Equation of this argument (S(RGBA) = Arg2)" src="images/topfrm2.png"/>


### -field D3DTOP_MODULATE

Multiply the components of the arguments. 

<img alt="Equation of the modulate operation (S(RGBA) = Arg1 x Arg 2)" src="images/topfrm3.png"/>


### -field D3DTOP_MODULATE2X

Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening. 

<img alt="Equation of the modulate2x operation (S(RGBA) = (Arg1 x Arg 2) then shift left 1)" src="images/topfrm4.png"/>


### -field D3DTOP_MODULATE4X

Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening. 

<img alt="Equation of the modulate4x operation (S(RGBA) = (Arg1 x Arg 2) then shift left 2)" src="images/topfrm5.png"/>


### -field D3DTOP_ADD

Add the components of the arguments. 

<img alt="Equation of the add operation (S(RGBA) = Arg1 + Arg 2)" src="images/topfrm6.png"/>


### -field D3DTOP_ADDSIGNED

Add the components of the arguments with a  - 0.5 bias, making the effective range of values from  - 0.5 through 0.5. 

<img alt="Equation of the add signed operation (S(RGBA) = Arg1 + Arg 2 – 0.5)" src="images/topfrm7.png"/>


### -field D3DTOP_ADDSIGNED2X

Add the components of the arguments with a  - 0.5 bias, and shift the products to the left 1 bit. 

<img alt="Equation of the add signed 2x operation ((S(RGBA) = Arg1 + Arg 2 - 0.5) then shift left 1)" src="images/topfrm8.png"/>


### -field D3DTOP_SUBTRACT

Subtract the components of the second argument from those of the first argument. 

<img alt="Equation of the subtract operation (S(RGBA) = Arg1 - Arg 2)" src="images/topfrm9.png"/>


### -field D3DTOP_ADDSMOOTH

Add the first and second arguments; then subtract their product from the sum. 

<img alt="Equation of the add smooth operation (S(RGBA) = Arg1 + Arg 2 x (1 - Arg1))" src="images/topfrm10.png"/>


### -field D3DTOP_BLENDDIFFUSEALPHA

Linearly blend this texture stage, using the interpolated alpha from each vertex. 

<img alt="Equation of the blend diffuse alpha operation (S(RGBA) = Arg1 x Alpha + Arg 2 x (1 - Alpha))" src="images/topfrm11.png"/>


### -field D3DTOP_BLENDTEXTUREALPHA

Linearly blend this texture stage, using the alpha from this stage's texture. 

<img alt="Equation of the blend texture alpha operation (S(RGBA) = Arg1 x Alpha + Arg 2 x (1 - Alpha))" src="images/topfrm11.png"/>


### -field D3DTOP_BLENDFACTORALPHA

Linearly blend this texture stage, using a scalar alpha set with the D3DRS_TEXTUREFACTOR render state. 

<img alt="Equation of the blend factor alpha operation (S(RGBA) = Arg1 x Alpha + Arg 2 x (1 - Alpha))" src="images/topfrm11.png"/>


### -field D3DTOP_BLENDTEXTUREALPHAPM

Linearly blend a texture stage that uses a premultiplied alpha. 

<img alt="Equation of the blend texture alpha PM operation (S(RGBA) = Arg1 + Arg 2 x (1 - Alpha))" src="images/topfrm12.png"/>


### -field D3DTOP_BLENDCURRENTALPHA

Linearly blend this texture stage, using the alpha taken from the previous texture stage. 

<img alt="Equation of the blend current alpha operation (S(RGBA) = Arg1 x Alpha + Arg2 x (1 - Alpha))" src="images/topfrm11.png"/>


### -field D3DTOP_PREMODULATE

D3DTOP_PREMODULATE is set in stage n. The output of stage n is arg1. Additionally, if there is a texture in stage n + 1, any D3DTA_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.


### -field D3DTOP_MODULATEALPHA_ADDCOLOR

Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one. This operation is supported only for color operations (D3DTSS_COLOROP). 

<img alt="Equation of the add color modulate alpha operation (S(RGBA) = Arg1(RGB) + Arg1(A) x Arg2(RGB))" src="images/topfrm13.png"/>


### -field D3DTOP_MODULATECOLOR_ADDALPHA

Modulate the arguments; then add the alpha of the first argument. This operation is supported only for color operations (D3DTSS_COLOROP). 

<img alt="Equation of the add alpha modulate color operation (S(RGBA) = Arg1(RGB) x Arg2(RGB) + Arg1(A))" src="images/topfrm14.png"/>


### -field D3DTOP_MODULATEINVALPHA_ADDCOLOR

Similar to D3DTOP_MODULATEALPHA_ADDCOLOR, but use the inverse of the alpha of the first argument. This operation is supported only for color operations (D3DTSS_COLOROP). 

<img alt="Equation of the add color modulate inverse alpha operation (S(RGBA) = (1 - Arg1(A)) x Arg2(RGB) + Arg1(RGB))" src="images/topfrm15.png"/>


### -field D3DTOP_MODULATEINVCOLOR_ADDALPHA

Similar to D3DTOP_MODULATECOLOR_ADDALPHA, but use the inverse of the color of the first argument. This operation is supported only for color operations (D3DTSS_COLOROP). 

<img alt="Equation of the add alpha modulate inverse color operation (S(RGBA) = (1 - Arg1(RGB)) x Arg2(RGB) + Arg1(A))" src="images/topfrm16.png"/>


### -field D3DTOP_BUMPENVMAP

Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance. This operation is supported only for color operations (D3DTSS_COLOROP). 


### -field D3DTOP_BUMPENVMAPLUMINANCE

Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance. This operation is supported only for color operations (D3DTSS_COLOROP). 


### -field D3DTOP_DOTPRODUCT3

 Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha. This operation is supported for color and alpha operations. 

<img alt="Equation of the dot product 3 operation (S(RGBA) = Arg1(R) x Arg2(R) + Arg1(G) x Arg2(G) + Arg1(B) x Arg2(B))" src="images/topfrm17.png"/>


    In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels. Also, note that as a color operation this does not updated the alpha it just updates the RGB components. 

However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default). You can also specify a separate scalar operation on the alpha channel. 


### -field D3DTOP_MULTIPLYADD

Performs a multiply-accumulate operation. It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result. 

S<sub>RGBA</sub> = Arg1 + Arg2 *  Arg3 


### -field D3DTOP_LERP

Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.

S<sub>RGBA</sub> = (Arg1) * 
    Arg2 + (1-
    Arg1) * 
    Arg3.


### -field D3DTOP_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 		


## -remarks




    
    The members of this type are used when setting color or alpha operations by using the D3DTSS_COLOROP or D3DTSS_ALPHAOP values with the <a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a> method.
    
    
    



    
    In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and 	Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments. Individual components of an argument are shown with subscripts. For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.
    





## -see-also




<a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

