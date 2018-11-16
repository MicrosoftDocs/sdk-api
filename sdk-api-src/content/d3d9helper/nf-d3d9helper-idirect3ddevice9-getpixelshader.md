---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShader
title: IDirect3DDevice9::GetPixelShader
author: windows-sdk-content
description: Retrieves the currently set pixel shader.
old-location: direct3d9\idirect3ddevice9__getpixelshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshader.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 77c70c81-d458-7302-5a4e-9899aad1f456, GetPixelShader, GetPixelShader method [Direct3D 9], GetPixelShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShader method, IDirect3DDevice9.GetPixelShader, IDirect3DDevice9::GetPixelShader, d3d9helper/IDirect3DDevice9::GetPixelShader, direct3d9.idirect3ddevice9__getpixelshader
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
 - IDirect3DDevice9.GetPixelShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DDevice9.GetPixelShader
: 
---

# IDirect3DDevice9::GetPixelShader


## -description


Retrieves the currently set pixel shader.


## -parameters




### -param ppShader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/b199544d-4617-4fe2-8a4a-d54fabd4d449">IDirect3DPixelShader9</a>**</b>

Pointer to a pixel shader interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method will not work on a device that is created using D3DCREATE_PUREDEVICE.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/bcc00274-7294-4c41-ac23-74b674bdfb77">IDirect3DDevice9::SetPixelShader</a>
 

 

