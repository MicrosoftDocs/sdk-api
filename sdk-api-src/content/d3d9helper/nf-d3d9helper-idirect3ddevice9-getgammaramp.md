---
UID: NF:d3d9helper.IDirect3DDevice9.GetGammaRamp
title: IDirect3DDevice9::GetGammaRamp (d3d9helper.h)
description: The IDirect3DDevice9::GetGammaRamp method (d3d9.h) retrieves the gamma correction ramp for the swap chain.
helpviewer_keywords: ["GetGammaRamp","GetGammaRamp method [Direct3D 9]","GetGammaRamp method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetGammaRamp method","IDirect3DDevice9.GetGammaRamp","IDirect3DDevice9::GetGammaRamp","b52b118d-254d-ca5b-efc0-a7e22cf186ef","d3d9helper/IDirect3DDevice9::GetGammaRamp","direct3d9.idirect3ddevice9__getgammaramp"]
old-location: direct3d9\idirect3ddevice9__getgammaramp.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getgammaramp.htm
ms.date: 08/11/2022
ms.keywords: GetGammaRamp, GetGammaRamp method [Direct3D 9], GetGammaRamp method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetGammaRamp method, IDirect3DDevice9.GetGammaRamp, IDirect3DDevice9::GetGammaRamp, b52b118d-254d-ca5b-efc0-a7e22cf186ef, d3d9helper/IDirect3DDevice9::GetGammaRamp, direct3d9.idirect3ddevice9__getgammaramp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::GetGammaRamp
 - d3d9helper/IDirect3DDevice9::GetGammaRamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetGammaRamp
---

# IDirect3DDevice9::GetGammaRamp


## -description

Retrieves the gamma correction ramp for the swap chain.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer specifying the swap chain.

### -param pRamp [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dgammaramp">D3DGAMMARAMP</a>*</b>

Pointer to an application-supplied <a href="/windows/desktop/direct3d9/d3dgammaramp">D3DGAMMARAMP</a> structure to fill with the gamma correction ramp.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setgammaramp">IDirect3DDevice9::SetGammaRamp</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>
