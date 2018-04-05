---
UID: NF:d3d9.IDirect3DDevice9.SetVertexShaderConstantI
title: IDirect3DDevice9::SetVertexShaderConstantI method
author: windows-driver-content
description: Sets an integer vertex shader constant.
old-location: direct3d9\idirect3ddevice9__setvertexshaderconstanti.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexshaderconstanti.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 10342244-afff-6fcd-2e64-c19547f2f547, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], SetVertexShaderConstantI method, IDirect3DDevice9::SetVertexShaderConstantI, SetVertexShaderConstantI method [Direct3D 9], SetVertexShaderConstantI method [Direct3D 9], IDirect3DDevice9 interface, SetVertexShaderConstantI,IDirect3DDevice9.SetVertexShaderConstantI, d3d9helper/IDirect3DDevice9::SetVertexShaderConstantI, direct3d9.idirect3ddevice9__setvertexshaderconstanti
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.SetVertexShaderConstantI
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetVertexShaderConstantI method


## -description


Sets an integer vertex shader constant.


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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

