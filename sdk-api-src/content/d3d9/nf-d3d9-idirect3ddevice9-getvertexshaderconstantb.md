---
UID: NF:d3d9.IDirect3DDevice9.GetVertexShaderConstantB
title: IDirect3DDevice9::GetVertexShaderConstantB
author: windows-sdk-content
description: Gets a Boolean vertex shader constant.
old-location: direct3d9\idirect3ddevice9__getvertexshaderconstantb.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getvertexshaderconstantb.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5d231bd1-6d2d-7685-724d-33578c0a400d, GetVertexShaderConstantB, GetVertexShaderConstantB method [Direct3D 9], GetVertexShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetVertexShaderConstantB method, IDirect3DDevice9.GetVertexShaderConstantB, IDirect3DDevice9::GetVertexShaderConstantB, d3d9helper/IDirect3DDevice9::GetVertexShaderConstantB, direct3d9.idirect3ddevice9__getvertexshaderconstantb
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
 - IDirect3DDevice9.GetVertexShaderConstantB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetVertexShaderConstantB


## -description


Gets a Boolean vertex shader constant.


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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

