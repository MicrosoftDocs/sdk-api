---
UID: NF:d3d9.IDirect3DDevice9.CreateVertexShader
title: IDirect3DDevice9::CreateVertexShader
author: windows-sdk-content
description: Creates a vertex shader.
old-location: direct3d9\idirect3ddevice9__createvertexshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvertexshader.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 42a56eab-a68f-232a-b21e-cc24c0b7b58d, CreateVertexShader, CreateVertexShader method [Direct3D 9], CreateVertexShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVertexShader method, IDirect3DDevice9.CreateVertexShader, IDirect3DDevice9::CreateVertexShader, d3d9helper/IDirect3DDevice9::CreateVertexShader, direct3d9.idirect3ddevice9__createvertexshader
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
 - IDirect3DDevice9.CreateVertexShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DDevice9.CreateVertexShader
: 
---

# IDirect3DDevice9::CreateVertexShader


## -description


Creates a vertex shader.


## -parameters




### -param pFunction [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to an array of tokens that represents the vertex shader, including any embedded debug and symbol table information. 
    


<ul>
<li>Use a function such as <a href="https://msdn.microsoft.com/9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8">D3DXCompileShader</a> to create the array from a HLSL shader.</li>
<li>Use a function like <a href="https://msdn.microsoft.com/24c3dcae-9397-4856-b072-0ae340157bf9">D3DXAssembleShader</a> to create the token array from an assembly language shader.</li>
<li>Use a function like <a href="https://msdn.microsoft.com/f34a2975-dcd5-4917-9b11-ed40583272f9">ID3DXEffectCompiler::CompileShader</a> to create the array from an effect.</li>
</ul>

### -param ppShader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>**</b>

Pointer to the returned vertex shader interface (see <a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



When a device is created, <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a> uses the behavior flag to determine whether to process vertices in hardware or software. There are three possibilities:

<ul>
<li>Process vertices in hardware by setting D3DCREATE_HARDWARE_VERTEXPROCESSING.</li>
<li>Process vertices in software by setting D3DCREATE_SOFTWARE_VERTEXPROCESSING.</li>
<li>Process vertices in either hardware or software by setting D3DCREATE_MIXED_VERTEXPROCESSING. To switch a mixed-mode device between software and hardware processing, use <a href="https://msdn.microsoft.com/05e67ec5-98f8-47c4-b5b7-aabb974db88a">IDirect3DDevice9::SetSoftwareVertexProcessing</a>.</li>
</ul>
For an example using <a href="https://msdn.microsoft.com/9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8">D3DXCompileShader</a>, see <a href="ac1492cf-d8aa-e22d-a7e0-dfd0a84d268d">HLSLwithoutEffects Sample</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

