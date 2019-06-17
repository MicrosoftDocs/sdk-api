---
UID: NF:d3d9.IDirect3DDevice9.GetPixelShaderConstantF
title: IDirect3DDevice9::GetPixelShaderConstantF (d3d9.h)
author: windows-sdk-content
description: Gets a floating-point shader constant.
old-location: direct3d9\idirect3ddevice9__getpixelshaderconstantf.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshaderconstantf.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 816b3869-d527-0369-a25d-c8da74027dff, GetPixelShaderConstantF, GetPixelShaderConstantF method [Direct3D 9], GetPixelShaderConstantF method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShaderConstantF method, IDirect3DDevice9.GetPixelShaderConstantF, IDirect3DDevice9::GetPixelShaderConstantF, d3d9helper/IDirect3DDevice9::GetPixelShaderConstantF, direct3d9.idirect3ddevice9__getpixelshaderconstantf
ms.topic: method
f1_keywords: ["d3d9/IDirect3DDevice9.GetPixelShaderConstantF"]
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
 - IDirect3DDevice9.GetPixelShaderConstantF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::GetPixelShaderConstantF


## -description


Gets a floating-point shader constant.


## -parameters




### -param StartRegister [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Register number that will contain the first constant value.


### -param pConstantData [in, out]

Type: <b>float*</b>

Pointer to an array of constants.


### -param Vector4fCount [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of four float vectors in the array of constants.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf">IDirect3DDevice9::SetPixelShaderConstantF</a>
 

 

