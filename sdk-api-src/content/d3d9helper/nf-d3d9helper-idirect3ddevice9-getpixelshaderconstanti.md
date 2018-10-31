---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShaderConstantI
title: IDirect3DDevice9::GetPixelShaderConstantI
author: windows-sdk-content
description: Gets an integer shader constant.
old-location: direct3d9\idirect3ddevice9__getpixelshaderconstanti.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshaderconstanti.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetPixelShaderConstantI, GetPixelShaderConstantI method [Direct3D 9], GetPixelShaderConstantI method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShaderConstantI method, IDirect3DDevice9.GetPixelShaderConstantI, IDirect3DDevice9::GetPixelShaderConstantI, d3d9helper/IDirect3DDevice9::GetPixelShaderConstantI, direct3d9.idirect3ddevice9__getpixelshaderconstanti, f6588a6e-ac30-9052-ae98-836dc602aab1
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
 - IDirect3DDevice9.GetPixelShaderConstantI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetPixelShaderConstantI


## -description


Gets an integer shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">int</a>*</b>

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



<a href="https://msdn.microsoft.com/en-us/library/Bb174453(v=VS.85).aspx">IDirect3DDevice9::SetPixelShaderConstantI</a>
 

 

