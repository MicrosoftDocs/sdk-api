---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShaderConstantB
title: IDirect3DDevice9::GetPixelShaderConstantB
author: windows-sdk-content
description: Gets a Boolean shader constant.
old-location: direct3d9\idirect3ddevice9__getpixelshaderconstantb.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshaderconstantb.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetPixelShaderConstantB, GetPixelShaderConstantB method [Direct3D 9], GetPixelShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShaderConstantB method, IDirect3DDevice9.GetPixelShaderConstantB, IDirect3DDevice9::GetPixelShaderConstantB, b5063da2-ebe9-220a-5bcc-e8d602dff035, d3d9helper/IDirect3DDevice9::GetPixelShaderConstantB, direct3d9.idirect3ddevice9__getpixelshaderconstantb
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
 - IDirect3DDevice9.GetPixelShaderConstantB
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetPixelShaderConstantB


## -description


Gets a Boolean shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Pointer to an array of constants.


### -param BoolCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of Boolean values in the array of constants.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/library/Bb174451(v=VS.85).aspx">IDirect3DDevice9::SetPixelShaderConstantB</a>
 

 

