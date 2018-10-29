---
UID: NF:d3d9.IDirect3DDevice9.SetTexture
title: IDirect3DDevice9::SetTexture
author: windows-sdk-content
description: Assigns a texture to a stage for a device.
old-location: direct3d9\idirect3ddevice9__settexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexture.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 30fa2907-7b07-b99a-b9b6-50d38166ea7d, IDirect3DDevice9 interface [Direct3D 9],SetTexture method, IDirect3DDevice9.SetTexture, IDirect3DDevice9::SetTexture, SetTexture, SetTexture method [Direct3D 9], SetTexture method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTexture, direct3d9.idirect3ddevice9__settexture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetTexture


## -description


Assigns a texture to a stage for a device.


## -parameters




### -param Stage

TBD


### -param pTexture [in]

Type: <b><a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a> interface, representing the texture being set. 



#### - Sampler [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero based sampler number.  Textures are bound to samplers; samplers define sampling state such as the filtering mode and the address wrapping mode. Textures are referenced differently by the programmable and the fixed function pipeline:
    


<ul>
<li>Programmable shaders reference textures using the sampler number. The number of samplers available to a programmable shader is dependent on the shader version. For vertex shaders, see <a href="https://msdn.microsoft.com/a4588ced-24e2-4d4e-93e4-35a985bafaa4">Sampler (Direct3D 9 asm-vs)</a>. For pixel shaders see <a href="https://msdn.microsoft.com/37cc28ae-fbd0-4f81-9e8e-f9609980d84e">Sampler (Direct3D 9 asm-ps)</a>.</li>
<li>The fixed function pipeline on the other hand, references textures by texture stage number. The maximum number of samplers is determined from two caps: MaxSimultaneousTextures and MaxTextureBlendStages of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure.</li>
</ul>
There are two other special cases for stage/sampler numbers.

<ul>
<li>A special number called D3DDMAPSAMPLER is used for <a href="https://msdn.microsoft.com/d6f16ff2-5a66-48a3-82c4-523faaafa6ae">Displacement Mapping (Direct3D 9)</a>.</li>
<li>A programmable vertex shader uses a special number defined by a <a href="https://msdn.microsoft.com/1347c3d6-67f6-4cea-9a93-9fc754755b47">D3DVERTEXTEXTURESAMPLER</a> when accessing <a href="https://msdn.microsoft.com/595cb5c0-da12-4fe9-944c-a61d8ed990b4">Vertex Textures in vs_3_0 (DirectX HLSL)</a>.</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



<b>SetTexture</b> is not allowed if the texture is created with a pool type of D3DPOOL_SCRATCH. <b>SetTexture</b> is not allowed with a pool type of D3DPOOL_SYSTEMMEM texture unless DevCaps is set with D3DDEVCAPS_TEXTURESYSTEMMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/f472de6f-6c46-4424-95e5-62164afaf026">GetTexture</a>



<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">GetTextureStageState</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">SetTextureStageState</a>
 

 

