---
UID: NF:d3d9.IDirect3DDevice9.SetPixelShaderConstantI
title: IDirect3DDevice9::SetPixelShaderConstantI
author: windows-sdk-content
description: Sets an integer shader constant.
old-location: direct3d9\idirect3ddevice9__setpixelshaderconstanti.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshaderconstanti.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPixelShaderConstantI method, IDirect3DDevice9.SetPixelShaderConstantI, IDirect3DDevice9::SetPixelShaderConstantI, SetPixelShaderConstantI, SetPixelShaderConstantI method [Direct3D 9], SetPixelShaderConstantI method [Direct3D 9],IDirect3DDevice9 interface, c9149cc8-7c91-43d6-390a-f416b94deaea, d3d9helper/IDirect3DDevice9::SetPixelShaderConstantI, direct3d9.idirect3ddevice9__setpixelshaderconstanti
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
 - IDirect3DDevice9.SetPixelShaderConstantI
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
- IDirect3DDevice9.SetPixelShaderConstantI
: 
---

# IDirect3DDevice9::SetPixelShaderConstantI


## -description


Sets an integer shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">int</a>*</b>

Pointer to an array of constants.


### -param Vector4iCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of four integer vectors in the array of constants.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174401(v=VS.85).aspx">IDirect3DDevice9::GetPixelShaderConstantI</a>
 

 

