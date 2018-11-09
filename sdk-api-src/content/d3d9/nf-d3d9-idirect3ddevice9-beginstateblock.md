---
UID: NF:d3d9.IDirect3DDevice9.BeginStateBlock
title: IDirect3DDevice9::BeginStateBlock
author: windows-sdk-content
description: Signals Direct3D to begin recording a device-state block.
old-location: direct3d9\idirect3ddevice9__beginstateblock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__beginstateblock.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 01991d00-eca6-e8db-e657-6432fe3184f2, BeginStateBlock, BeginStateBlock method [Direct3D 9], BeginStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],BeginStateBlock method, IDirect3DDevice9.BeginStateBlock, IDirect3DDevice9::BeginStateBlock, d3d9helper/IDirect3DDevice9::BeginStateBlock, direct3d9.idirect3ddevice9__beginstateblock
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
 - IDirect3DDevice9.BeginStateBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::BeginStateBlock


## -description


Signals Direct3D to begin recording a device-state block.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.




## -remarks



Applications can ensure that all recorded states are valid by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb205859(v=VS.85).aspx">IDirect3DDevice9::ValidateDevice</a> method prior to calling this method.

The following methods can be recorded in a state block, after calling <b>IDirect3DDevice9::BeginStateBlock</b> and before <a href="https://msdn.microsoft.com/en-us/library/Bb174376(v=VS.85).aspx">IDirect3DDevice9::EndStateBlock</a>. 

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174421(v=VS.85).aspx">IDirect3DDevice9::LightEnable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174426(v=VS.85).aspx">IDirect3DDevice9::SetClipPlane</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174428(v=VS.85).aspx">IDirect3DDevice9::SetCurrentTexturePalette</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174433(v=VS.85).aspx">IDirect3DDevice9::SetFVF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174435(v=VS.85).aspx">IDirect3DDevice9::SetIndices</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174436(v=VS.85).aspx">IDirect3DDevice9::SetLight</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174437(v=VS.85).aspx">IDirect3DDevice9::SetMaterial</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174438(v=VS.85).aspx">IDirect3DDevice9::SetNPatchMode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174450(v=VS.85).aspx">IDirect3DDevice9::SetPixelShader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174451(v=VS.85).aspx">IDirect3DDevice9::SetPixelShaderConstantB</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174452(v=VS.85).aspx">IDirect3DDevice9::SetPixelShaderConstantF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174453(v=VS.85).aspx">IDirect3DDevice9::SetPixelShaderConstantI</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174454(v=VS.85).aspx">IDirect3DDevice9::SetRenderState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174456(v=VS.85).aspx">IDirect3DDevice9::SetSamplerState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174457(v=VS.85).aspx">IDirect3DDevice9::SetScissorRect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174459(v=VS.85).aspx">IDirect3DDevice9::SetStreamSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174460(v=VS.85).aspx">IDirect3DDevice9::SetStreamSourceFreq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174461(v=VS.85).aspx">IDirect3DDevice9::SetTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174462(v=VS.85).aspx">IDirect3DDevice9::SetTextureStageState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174463(v=VS.85).aspx">IDirect3DDevice9::SetTransform</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174469(v=VS.85).aspx">IDirect3DDevice9::SetViewport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">IDirect3DDevice9::SetVertexDeclaration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174465(v=VS.85).aspx">IDirect3DDevice9::SetVertexShader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174466(v=VS.85).aspx">IDirect3DDevice9::SetVertexShaderConstantB</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174467(v=VS.85).aspx">IDirect3DDevice9::SetVertexShaderConstantF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174468(v=VS.85).aspx">IDirect3DDevice9::SetVertexShaderConstantI</a>
</li>
</ul>
The ordering of state changes in a state block is not guaranteed. If the same state is specified multiple times in a state block, only the last value is used.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174362(v=VS.85).aspx">IDirect3DDevice9::CreateStateBlock</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174376(v=VS.85).aspx">IDirect3DDevice9::EndStateBlock</a>
 

 

