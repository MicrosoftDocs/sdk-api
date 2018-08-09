---
UID: NF:d3d9helper.IDirect3DDevice9.SetTexture
title: IDirect3DDevice9::SetTexture
author: windows-sdk-content
description: Assigns a texture to a stage for a device.
old-location: direct3d9\idirect3ddevice9__settexture.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexture.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 30fa2907-7b07-b99a-b9b6-50d38166ea7d, IDirect3DDevice9 interface [Direct3D 9],SetTexture method, IDirect3DDevice9.SetTexture, IDirect3DDevice9::SetTexture, SetTexture, SetTexture method [Direct3D 9], SetTexture method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTexture, direct3d9.idirect3ddevice9__settexture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetTexture
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetTexture


## -description


Assigns a texture to a stage for a device.


## -parameters




### -param Stage




### -param pTexture [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface, representing the texture being set. 



#### - Sampler [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero based sampler number.  Textures are bound to samplers; samplers define sampling state such as the filtering mode and the address wrapping mode. Textures are referenced differently by the programmable and the fixed function pipeline:
    


<ul>
<li>Programmable shaders reference textures using the sampler number. The number of samplers available to a programmable shader is dependent on the shader version. For vertex shaders, see <a href="https://msdn.microsoft.com/en-us/library/Bb172957(v=VS.85).aspx">Sampler (Direct3D 9 asm-vs)</a>. For pixel shaders see <a href="https://msdn.microsoft.com/en-us/library/Bb172922(v=VS.85).aspx">Sampler (Direct3D 9 asm-ps)</a>.</li>
<li>The fixed function pipeline on the other hand, references textures by texture stage number. The maximum number of samplers is determined from two caps: MaxSimultaneousTextures and MaxTextureBlendStages of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure.</li>
</ul>
There are two other special cases for stage/sampler numbers.

<ul>
<li>A special number called D3DDMAPSAMPLER is used for <a href="https://msdn.microsoft.com/en-us/library/Bb219748(v=VS.85).aspx">Displacement Mapping (Direct3D 9)</a>.</li>
<li>A programmable vertex shader uses a special number defined by a <a href="https://msdn.microsoft.com/en-us/library/Bb172631(v=VS.85).aspx">D3DVERTEXTEXTURESAMPLER</a> when accessing <a href="https://msdn.microsoft.com/en-us/library/Bb206339(v=VS.85).aspx">Vertex Textures in vs_3_0 (DirectX HLSL)</a>.</li>
</ul>

## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



<b>SetTexture</b> is not allowed if the texture is created with a pool type of D3DPOOL_SCRATCH. <b>SetTexture</b> is not allowed with a pool type of D3DPOOL_SYSTEMMEM texture unless DevCaps is set with D3DDEVCAPS_TEXTURESYSTEMMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174412(v=VS.85).aspx">GetTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174413(v=VS.85).aspx">GetTextureStageState</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174462(v=VS.85).aspx">SetTextureStageState</a>
 

 

