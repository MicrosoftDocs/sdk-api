---
UID: NF:d3d9helper.IDirect3DDevice9.SetPixelShaderConstantB
title: IDirect3DDevice9::SetPixelShaderConstantB
author: windows-sdk-content
description: Sets a Boolean shader constant.
old-location: direct3d9\idirect3ddevice9__setpixelshaderconstantb.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshaderconstantb.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPixelShaderConstantB method, IDirect3DDevice9.SetPixelShaderConstantB, IDirect3DDevice9::SetPixelShaderConstantB, SetPixelShaderConstantB, SetPixelShaderConstantB method [Direct3D 9], SetPixelShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetPixelShaderConstantB, dcb060c3-b816-f722-dc79-1f7a1f30e4b9, direct3d9.idirect3ddevice9__setpixelshaderconstantb
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
 - IDirect3DDevice9.SetPixelShaderConstantB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/fe32886b-f50c-47a6-b854-a96f53fd92b4">IDirect3DDevice9::GetPixelShaderConstantB</a>
 

 

