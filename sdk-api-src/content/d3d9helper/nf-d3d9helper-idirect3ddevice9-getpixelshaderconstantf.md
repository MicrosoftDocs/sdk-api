---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShaderConstantF
title: IDirect3DDevice9::GetPixelShaderConstantF
author: windows-sdk-content
description: Gets a floating-point shader constant.
old-location: direct3d9\idirect3ddevice9__getpixelshaderconstantf.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshaderconstantf.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 816b3869-d527-0369-a25d-c8da74027dff, GetPixelShaderConstantF, GetPixelShaderConstantF method [Direct3D 9], GetPixelShaderConstantF method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShaderConstantF method, IDirect3DDevice9.GetPixelShaderConstantF, IDirect3DDevice9::GetPixelShaderConstantF, d3d9helper/IDirect3DDevice9::GetPixelShaderConstantF, direct3d9.idirect3ddevice9__getpixelshaderconstantf
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
 - IDirect3DDevice9.GetPixelShaderConstantF
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetPixelShaderConstantF


## -description


Gets a floating-point shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in, out]

Type: <b>float*</b>

Pointer to an array of constants.


### -param Vector4fCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of four float vectors in the array of constants.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/17f68eb6-254c-4457-98ea-4a76ee1823ac">IDirect3DDevice9::SetPixelShaderConstantF</a>
 

 

