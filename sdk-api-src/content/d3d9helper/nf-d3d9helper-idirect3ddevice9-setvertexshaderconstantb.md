---
UID: NF:d3d9helper.IDirect3DDevice9.SetVertexShaderConstantB
title: IDirect3DDevice9::SetVertexShaderConstantB
author: windows-sdk-content
description: Sets a Boolean vertex shader constant.
old-location: direct3d9\idirect3ddevice9__setvertexshaderconstantb.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexshaderconstantb.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetVertexShaderConstantB method, IDirect3DDevice9.SetVertexShaderConstantB, IDirect3DDevice9::SetVertexShaderConstantB, SetVertexShaderConstantB, SetVertexShaderConstantB method [Direct3D 9], SetVertexShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, aa9539bc-215f-a118-f03d-530e7ea6514d, d3d9helper/IDirect3DDevice9::SetVertexShaderConstantB, direct3d9.idirect3ddevice9__setvertexshaderconstantb
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.SetVertexShaderConstantB
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetVertexShaderConstantB


## -description


Sets a Boolean vertex shader constant.


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
 

 

