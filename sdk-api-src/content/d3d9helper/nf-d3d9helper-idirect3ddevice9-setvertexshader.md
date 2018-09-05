---
UID: NF:d3d9helper.IDirect3DDevice9.SetVertexShader
title: IDirect3DDevice9::SetVertexShader
author: windows-sdk-content
description: Sets the vertex shader.
old-location: direct3d9\idirect3ddevice9__setvertexshader.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexshader.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 4fecc980-501f-804d-d212-782bd9df73d4, IDirect3DDevice9 interface [Direct3D 9],SetVertexShader method, IDirect3DDevice9.SetVertexShader, IDirect3DDevice9::SetVertexShader, SetVertexShader, SetVertexShader method [Direct3D 9], SetVertexShader method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetVertexShader, direct3d9.idirect3ddevice9__setvertexshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
 - IDirect3DDevice9.SetVertexShader
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetVertexShader


## -description


Sets the vertex shader.


## -parameters




### -param pShader [in]

Type: <b><a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>*</b>

Vertex shader interface. For more information, see <a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



To set a fixed-function vertex shader (after having set a programmable vertex shader), call <b>IDirect3DDevice9::SetVertexShader</b>(NULL) to release the programmable shader, and then call <a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a> with the fixed-function vertex format.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/9c33415b-960a-4f55-a497-b30d0525cf3f">IDirect3DDevice9::GetVertexShader</a>
 

 

