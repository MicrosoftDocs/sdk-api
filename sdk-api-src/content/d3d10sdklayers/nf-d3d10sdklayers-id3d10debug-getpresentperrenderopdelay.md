---
UID: NF:d3d10sdklayers.ID3D10Debug.GetPresentPerRenderOpDelay
title: ID3D10Debug::GetPresentPerRenderOpDelay (d3d10sdklayers.h)
description: Get the number of milliseconds to sleep after Present is called.
helpviewer_keywords: ["089e85a9-c0e8-518c-4ced-8dfac65c1761","GetPresentPerRenderOpDelay","GetPresentPerRenderOpDelay method [Direct3D 10]","GetPresentPerRenderOpDelay method [Direct3D 10]","ID3D10Debug interface","ID3D10Debug interface [Direct3D 10]","GetPresentPerRenderOpDelay method","ID3D10Debug.GetPresentPerRenderOpDelay","ID3D10Debug::GetPresentPerRenderOpDelay","d3d10sdklayers/ID3D10Debug::GetPresentPerRenderOpDelay","direct3d10.id3d10debug_getpresentperrenderopdelay"]
old-location: direct3d10\id3d10debug_getpresentperrenderopdelay.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_getpresentperrenderopdelay.htm
ms.date: 12/05/2018
ms.keywords: 089e85a9-c0e8-518c-4ced-8dfac65c1761, GetPresentPerRenderOpDelay, GetPresentPerRenderOpDelay method [Direct3D 10], GetPresentPerRenderOpDelay method [Direct3D 10],ID3D10Debug interface, ID3D10Debug interface [Direct3D 10],GetPresentPerRenderOpDelay method, ID3D10Debug.GetPresentPerRenderOpDelay, ID3D10Debug::GetPresentPerRenderOpDelay, d3d10sdklayers/ID3D10Debug::GetPresentPerRenderOpDelay, direct3d10.id3d10debug_getpresentperrenderopdelay
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
 - ID3D10Debug::GetPresentPerRenderOpDelay
 - d3d10sdklayers/ID3D10Debug::GetPresentPerRenderOpDelay
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
 - ID3D10Debug.GetPresentPerRenderOpDelay
---

# ID3D10Debug::GetPresentPerRenderOpDelay


## -description

Get the number of milliseconds to sleep after <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a> is called.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of milliseconds to sleep after Present is called.

## -remarks

Value is set with <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay">ID3D10Debug::SetPresentPerRenderOpDelay</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10debug">ID3D10Debug Interface</a>
