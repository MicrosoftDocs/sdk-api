---
UID: NF:d3d9helper.IDirect3DDevice9.SetPixelShader
title: IDirect3DDevice9::SetPixelShader
author: windows-sdk-content
description: Sets the current pixel shader to a previously created pixel shader.
old-location: direct3d9\idirect3ddevice9__setpixelshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshader.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPixelShader method, IDirect3DDevice9.SetPixelShader, IDirect3DDevice9::SetPixelShader, SetPixelShader, SetPixelShader method [Direct3D 9], SetPixelShader method [Direct3D 9],IDirect3DDevice9 interface, c65d883e-77d2-f541-2bd4-48dba090930c, d3d9helper/IDirect3DDevice9::SetPixelShader, direct3d9.idirect3ddevice9__setpixelshader
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
 - IDirect3DDevice9.SetPixelShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetPixelShader


## -description


Sets the current pixel shader to a previously created pixel shader.


## -parameters




### -param pShader [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205869(v=VS.85).aspx">IDirect3DPixelShader9</a>*</b>

Pixel shader interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174398(v=VS.85).aspx">IDirect3DDevice9::GetPixelShader</a>
 

 

