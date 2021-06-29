---
UID: NF:d3d11sdklayers.ID3D11Debug.GetPresentPerRenderOpDelay
title: ID3D11Debug::GetPresentPerRenderOpDelay (d3d11sdklayers.h)
description: Get the number of milliseconds to sleep after IDXGISwapChain::Present is called.
helpviewer_keywords: ["GetPresentPerRenderOpDelay","GetPresentPerRenderOpDelay method [Direct3D 11]","GetPresentPerRenderOpDelay method [Direct3D 11]","ID3D11Debug interface","ID3D11Debug interface [Direct3D 11]","GetPresentPerRenderOpDelay method","ID3D11Debug.GetPresentPerRenderOpDelay","ID3D11Debug::GetPresentPerRenderOpDelay","d3d11sdklayers/ID3D11Debug::GetPresentPerRenderOpDelay","d80fb328-cbcf-b755-35cd-3ac7f39aeff8","direct3d11.id3d11debug_getpresentperrenderopdelay"]
old-location: direct3d11\id3d11debug_getpresentperrenderopdelay.htm
tech.root: direct3d11
ms.assetid: 7c55f370-df9c-40d5-97d8-6e25cb9e5579
ms.date: 12/05/2018
ms.keywords: GetPresentPerRenderOpDelay, GetPresentPerRenderOpDelay method [Direct3D 11], GetPresentPerRenderOpDelay method [Direct3D 11],ID3D11Debug interface, ID3D11Debug interface [Direct3D 11],GetPresentPerRenderOpDelay method, ID3D11Debug.GetPresentPerRenderOpDelay, ID3D11Debug::GetPresentPerRenderOpDelay, d3d11sdklayers/ID3D11Debug::GetPresentPerRenderOpDelay, d80fb328-cbcf-b755-35cd-3ac7f39aeff8, direct3d11.id3d11debug_getpresentperrenderopdelay
req.header: d3d11sdklayers.h
req.include-header: 
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Debug::GetPresentPerRenderOpDelay
 - d3d11sdklayers/ID3D11Debug::GetPresentPerRenderOpDelay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Debug.GetPresentPerRenderOpDelay
---

# ID3D11Debug::GetPresentPerRenderOpDelay


## -description

Get the number of milliseconds to sleep after <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> is called.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of milliseconds to sleep after Present is called.

## -remarks

Value is set with <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay">ID3D11Debug::SetPresentPerRenderOpDelay</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11debug">ID3D11Debug Interface</a>
