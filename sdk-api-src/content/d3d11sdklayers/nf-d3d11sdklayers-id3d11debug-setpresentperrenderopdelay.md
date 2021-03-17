---
UID: NF:d3d11sdklayers.ID3D11Debug.SetPresentPerRenderOpDelay
title: ID3D11Debug::SetPresentPerRenderOpDelay (d3d11sdklayers.h)
description: Set the number of milliseconds to sleep after IDXGISwapChain::Present is called.
helpviewer_keywords: ["573cbcb7-dbec-80ce-3edb-e1d60b5c1261","ID3D11Debug interface [Direct3D 11]","SetPresentPerRenderOpDelay method","ID3D11Debug.SetPresentPerRenderOpDelay","ID3D11Debug::SetPresentPerRenderOpDelay","SetPresentPerRenderOpDelay","SetPresentPerRenderOpDelay method [Direct3D 11]","SetPresentPerRenderOpDelay method [Direct3D 11]","ID3D11Debug interface","d3d11sdklayers/ID3D11Debug::SetPresentPerRenderOpDelay","direct3d11.id3d11debug_setpresentperrenderopdelay"]
old-location: direct3d11\id3d11debug_setpresentperrenderopdelay.htm
tech.root: direct3d11
ms.assetid: 72489871-819a-4f75-a3ad-03f93f5c7761
ms.date: 12/05/2018
ms.keywords: 573cbcb7-dbec-80ce-3edb-e1d60b5c1261, ID3D11Debug interface [Direct3D 11],SetPresentPerRenderOpDelay method, ID3D11Debug.SetPresentPerRenderOpDelay, ID3D11Debug::SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay method [Direct3D 11], SetPresentPerRenderOpDelay method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::SetPresentPerRenderOpDelay, direct3d11.id3d11debug_setpresentperrenderopdelay
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
 - ID3D11Debug::SetPresentPerRenderOpDelay
 - d3d11sdklayers/ID3D11Debug::SetPresentPerRenderOpDelay
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
 - ID3D11Debug.SetPresentPerRenderOpDelay
---

# ID3D11Debug::SetPresentPerRenderOpDelay


## -description

Set the number of milliseconds to sleep after <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> is called.

## -parameters

### -param Milliseconds

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of milliseconds to sleep after Present is called.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The application will only sleep if D3D11_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is a set in the <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask">feature mask</a>. If that flag is not set the number of milliseconds is set but ignored and the application does not sleep. 10ms is used as a default value if this method is never called.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11debug">ID3D11Debug Interface</a>