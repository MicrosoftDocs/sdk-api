---
UID: NF:d3d10sdklayers.ID3D10Debug.SetPresentPerRenderOpDelay
title: ID3D10Debug::SetPresentPerRenderOpDelay (d3d10sdklayers.h)
description: Set the number of milliseconds to sleep after Present is called.
helpviewer_keywords: ["42cc51c9-dccb-4b3d-9dcc-643abb49543f","ID3D10Debug interface [Direct3D 10]","SetPresentPerRenderOpDelay method","ID3D10Debug.SetPresentPerRenderOpDelay","ID3D10Debug::SetPresentPerRenderOpDelay","SetPresentPerRenderOpDelay","SetPresentPerRenderOpDelay method [Direct3D 10]","SetPresentPerRenderOpDelay method [Direct3D 10]","ID3D10Debug interface","d3d10sdklayers/ID3D10Debug::SetPresentPerRenderOpDelay","direct3d10.id3d10debug_setpresentperrenderopdelay"]
old-location: direct3d10\id3d10debug_setpresentperrenderopdelay.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setpresentperrenderopdelay.htm
ms.date: 12/05/2018
ms.keywords: 42cc51c9-dccb-4b3d-9dcc-643abb49543f, ID3D10Debug interface [Direct3D 10],SetPresentPerRenderOpDelay method, ID3D10Debug.SetPresentPerRenderOpDelay, ID3D10Debug::SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay method [Direct3D 10], SetPresentPerRenderOpDelay method [Direct3D 10],ID3D10Debug interface, d3d10sdklayers/ID3D10Debug::SetPresentPerRenderOpDelay, direct3d10.id3d10debug_setpresentperrenderopdelay
req.header: d3d10sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Debug::SetPresentPerRenderOpDelay
 - d3d10sdklayers/ID3D10Debug::SetPresentPerRenderOpDelay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetPresentPerRenderOpDelay
---

# ID3D10Debug::SetPresentPerRenderOpDelay


## -description

Set the number of milliseconds to sleep after <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a> is called.

## -parameters

### -param Milliseconds [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of milliseconds to sleep after Present is called.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The application will only sleep if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is a set in the <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask">feature mask</a>. If that flag is not set the number of milliseconds is set but ignored and the application does not sleep. 10ms is used as a default value if this method is never called.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10debug">ID3D10Debug Interface</a>