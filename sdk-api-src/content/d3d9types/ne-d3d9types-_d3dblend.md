---
UID: NE:d3d9types._D3DBLEND
title: "_D3DBLEND"
author: windows-driver-content
description: Defines the supported blend mode.
old-location: direct3d9\D3DBLEND.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dblend.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 1b09f110-7ab3-1271-0f41-9e61559fe04e, D3DBLEND, D3DBLEND enumeration [Direct3D 9], D3DBLEND_BLENDFACTOR, D3DBLEND_BOTHINVSRCALPHA, D3DBLEND_BOTHSRCALPHA, D3DBLEND_DESTALPHA, D3DBLEND_DESTCOLOR, D3DBLEND_FORCE_DWORD, D3DBLEND_INVBLENDFACTOR, D3DBLEND_INVDESTALPHA, D3DBLEND_INVDESTCOLOR, D3DBLEND_INVSRCALPHA, D3DBLEND_INVSRCCOLOR, D3DBLEND_INVSRCCOLOR2, D3DBLEND_ONE, D3DBLEND_SRCALPHA, D3DBLEND_SRCALPHASAT, D3DBLEND_SRCCOLOR, D3DBLEND_SRCCOLOR2, D3DBLEND_ZERO, LPD3DBLEND, LPD3DBLEND enumeration pointer [Direct3D 9], _D3DBLEND, d3d9types/D3DBLEND, d3d9types/D3DBLEND_BLENDFACTOR, d3d9types/D3DBLEND_BOTHINVSRCALPHA, d3d9types/D3DBLEND_BOTHSRCALPHA, d3d9types/D3DBLEND_DESTALPHA, d3d9types/D3DBLEND_DESTCOLOR, d3d9types/D3DBLEND_FORCE_DWORD, d3d9types/D3DBLEND_INVBLENDFACTOR, d3d9types/D3DBLEND_INVDESTALPHA, d3d9types/D3DBLEND_INVDESTCOLOR, d3d9types/D3DBLEND_INVSRCALPHA, d3d9types/D3DBLEND_INVSRCCOLOR, d3d9types/D3DBLEND_INVSRCCOLOR2, d3d9types/D3DBLEND_ONE, d3d9types/D3DBLEND_SRCALPHA, d3d9types/D3DBLEND_SRCALPHASAT, d3d9types/D3DBLEND_SRCCOLOR, d3d9types/D3DBLEND_SRCCOLOR2, d3d9types/D3DBLEND_ZERO, d3d9types/LPD3DBLEND, direct3d9.D3DBLEND
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
req.typenames: D3DBLEND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DBLEND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBLEND enumeration


## -description


Defines the supported blend mode.


## -enum-fields




### -field D3DBLEND_ZERO

Blend factor is (0, 0, 0, 0). 


### -field D3DBLEND_ONE

Blend factor is (1, 1, 1, 1). 


### -field D3DBLEND_SRCCOLOR

Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ). 


### -field D3DBLEND_INVSRCCOLOR

Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ). 


### -field D3DBLEND_SRCALPHA

Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ). 


### -field D3DBLEND_INVSRCALPHA

Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ). 


### -field D3DBLEND_DESTALPHA

Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>). 


### -field D3DBLEND_INVDESTALPHA

Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>). 


### -field D3DBLEND_DESTCOLOR

Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>). 


### -field D3DBLEND_INVDESTCOLOR

Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>). 


### -field D3DBLEND_SRCALPHASAT

Blend factor is (f, f, f, 1); where f = min(Aₛ, 1
    - A<sub>d</sub>). 


### -field D3DBLEND_BOTHSRCALPHA

<b>Obsolete</b>. Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND_SRCALPHA and D3DBLEND_INVSRCALPHA in separate calls. 


### -field D3DBLEND_BOTHINVSRCALPHA

<b>Obsolete</b>. Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden. This blend mode is supported only for the D3DRS_SRCBLEND render state. 


### -field D3DBLEND_BLENDFACTOR

Constant color blending factor used by the frame-buffer blender. This blend mode is supported only if D3DPBLENDCAPS_BLENDFACTOR is set in the <b>SrcBlendCaps</b> or <b>DestBlendCaps</b> members of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>.


### -field D3DBLEND_INVBLENDFACTOR

Inverted constant color-blending factor used by the frame-buffer blender. This blend mode is supported only if the D3DPBLENDCAPS_BLENDFACTOR bit is set in the <b>SrcBlendCaps</b> or <b>DestBlendCaps</b> members of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>.


### -field D3DBLEND_SRCCOLOR2

Blend factor is (PSOutColor[1]<sub>r</sub>, PSOutColor[1]<sub>g</sub>, PSOutColor[1]<sub>b</sub>, not used). See <a href="https://docs.microsoft.com/">Render Target Blending</a>.



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

This flag is available in Direct3D 9Ex only.

</td>
</tr>
</table>
 


### -field D3DBLEND_INVSRCCOLOR2

Blend factor is (1 - PSOutColor[1]<sub>r</sub>, 1 - PSOutColor[1]<sub>g</sub>, 1 - PSOutColor[1]<sub>b</sub>, not used)). See <a href="https://docs.microsoft.com/">Render Target Blending</a>.



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

This flag is available in Direct3D 9Ex only.

</td>
</tr>
</table>
 


### -field D3DBLEND_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.

The values in this enumerated type are used by the following render states:

<ul>
<li>D3DRS_DESTBLEND</li>
<li>D3DRS_SRCBLEND</li>
<li>D3DRS_DESTBLENDALPHA</li>
<li>D3DRS_SRCBLENDALPHA</li>
</ul>
See <a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>


<h3><a id="Render_Target_Blending"></a><a id="render_target_blending"></a><a id="RENDER_TARGET_BLENDING"></a>Render Target Blending</h3>
Direct3D 9Ex has improved text rendering capabilities. Rendering clear-type fonts would normally require two passes. To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor[0] and PSOutColor[1]. The first color would contain the standard 3 color components (RGB). The second color would contain 3 alpha components (one for each component of the first color).

These new blending modes are only used for text rendering on the first render target.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

