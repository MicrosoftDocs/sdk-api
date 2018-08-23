---
UID: NF:d3d9helper.IDirect3DDevice9.SetPixelShaderConstantB
title: IDirect3DDevice9::SetPixelShaderConstantB
author: windows-sdk-content
description: Sets a Boolean shader constant.
old-location: direct3d9\idirect3ddevice9__setpixelshaderconstantb.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshaderconstantb.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPixelShaderConstantB method, IDirect3DDevice9.SetPixelShaderConstantB, IDirect3DDevice9::SetPixelShaderConstantB, SetPixelShaderConstantB, SetPixelShaderConstantB method [Direct3D 9], SetPixelShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetPixelShaderConstantB, dcb060c3-b816-f722-dc79-1f7a1f30e4b9, direct3d9.idirect3ddevice9__setpixelshaderconstantb
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
 - IDirect3DDevice9.SetPixelShaderConstantB
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetPixelShaderConstantB


## -description


Sets a Boolean shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Pointer to an array of constants.


### -param BoolCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of boolean values in the array of constants.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174399(v=VS.85).aspx">IDirect3DDevice9::GetPixelShaderConstantB</a>
 

 

