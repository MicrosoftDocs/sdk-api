---
UID: NF:d3d9helper.IDirect3DDevice9.BeginStateBlock
title: IDirect3DDevice9::BeginStateBlock
author: windows-sdk-content
description: Signals Direct3D to begin recording a device-state block.
old-location: direct3d9\idirect3ddevice9__beginstateblock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__beginstateblock.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 01991d00-eca6-e8db-e657-6432fe3184f2, BeginStateBlock, BeginStateBlock method [Direct3D 9], BeginStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],BeginStateBlock method, IDirect3DDevice9.BeginStateBlock, IDirect3DDevice9::BeginStateBlock, d3d9helper/IDirect3DDevice9::BeginStateBlock, direct3d9.idirect3ddevice9__beginstateblock
ms.prod: windows-hardware
ms.technology: windows-devices
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.




## -remarks



Applications can ensure that all recorded states are valid by calling the <a href="https://msdn.microsoft.com/2ae81f51-fa31-4d8a-88a0-f271a76e082b">IDirect3DDevice9::ValidateDevice</a> method prior to calling this method.

The following methods can be recorded in a state block, after calling <b>IDirect3DDevice9::BeginStateBlock</b> and before <a href="https://msdn.microsoft.com/170fab09-671f-4faf-99e4-849ba4a53688">IDirect3DDevice9::EndStateBlock</a>. 

<ul>
<li>
<a href="https://msdn.microsoft.com/3a23a10b-ded5-4dfc-ac17-ebe199f9a788">IDirect3DDevice9::LightEnable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e5a7f085-6a69-4da8-9c3a-a7c546c10514">IDirect3DDevice9::SetClipPlane</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5d97ccf4-20cd-4773-905a-e12b279e4f0b">IDirect3DDevice9::SetCurrentTexturePalette</a>
</li>
<li>
<a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b27403da-9079-4f97-8520-c2617b53e059">IDirect3DDevice9::SetIndices</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1f07ba6-8a9f-4bac-8dad-16160559fa4c">IDirect3DDevice9::SetLight</a>
</li>
<li>
<a href="https://msdn.microsoft.com/52cdcd0c-1cc9-4849-91e2-822414f7f186">IDirect3DDevice9::SetMaterial</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab5a1cfd-0c37-471c-af27-4ae078b8f7cd">IDirect3DDevice9::SetNPatchMode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bcc00274-7294-4c41-ac23-74b674bdfb77">IDirect3DDevice9::SetPixelShader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/69e44683-a551-4503-8246-c22423092734">IDirect3DDevice9::SetPixelShaderConstantB</a>
</li>
<li>
<a href="https://msdn.microsoft.com/17f68eb6-254c-4457-98ea-4a76ee1823ac">IDirect3DDevice9::SetPixelShaderConstantF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/da71a62b-016d-4c3c-8fa7-23c5e349c5fe">IDirect3DDevice9::SetPixelShaderConstantI</a>
</li>
<li>
<a href="https://msdn.microsoft.com/65738aae-aa90-48c5-8c9c-1927d1c92c54">IDirect3DDevice9::SetRenderState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ea215b7-eda1-4538-a5b8-6bbbb692494c">IDirect3DDevice9::SetScissorRect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/15f4cbf8-7f14-4905-b32e-ed253bc0a3de">IDirect3DDevice9::SetStreamSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12fdf57b-25c6-4896-b0a2-931b1a546c35">IDirect3DDevice9::SetStreamSourceFreq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ec62aeee-037f-4c33-b242-e0483872016c">IDirect3DDevice9::SetTexture</a>
</li>
<li>
<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">IDirect3DDevice9::SetTransform</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57fd3a83-4bb4-4f6c-9233-d65208d4bb39">IDirect3DDevice9::SetViewport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">IDirect3DDevice9::SetVertexDeclaration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e4913fd8-5cb3-4799-8c91-d39f213d4b47">IDirect3DDevice9::SetVertexShader</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3a781645-e622-415c-88ce-8c768ac602d5">IDirect3DDevice9::SetVertexShaderConstantB</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2d3f206f-2951-4a32-91cc-2b579cc630d0">IDirect3DDevice9::SetVertexShaderConstantF</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d244d8c0-065b-4d88-9c0a-1610e518e887">IDirect3DDevice9::SetVertexShaderConstantI</a>
</li>
</ul>
The ordering of state changes in a state block is not guaranteed. If the same state is specified multiple times in a state block, only the last value is used.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/36951221-ab14-45bc-bfb3-4294e3d20fb0">IDirect3DDevice9::CreateStateBlock</a>



<a href="https://msdn.microsoft.com/170fab09-671f-4faf-99e4-849ba4a53688">IDirect3DDevice9::EndStateBlock</a>
 

 

