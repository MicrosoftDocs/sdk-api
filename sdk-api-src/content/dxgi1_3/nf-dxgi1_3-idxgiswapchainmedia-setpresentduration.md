---
UID: NF:dxgi1_3.IDXGISwapChainMedia.SetPresentDuration
title: IDXGISwapChainMedia::SetPresentDuration (dxgi1_3.h)
description: Requests a custom presentation duration (custom refresh rate).
helpviewer_keywords: ["IDXGISwapChainMedia interface [DXGI]","SetPresentDuration method","IDXGISwapChainMedia.SetPresentDuration","IDXGISwapChainMedia::SetPresentDuration","SetPresentDuration","SetPresentDuration method [DXGI]","SetPresentDuration method [DXGI]","IDXGISwapChainMedia interface","direct3ddxgi.idxgiswapchainmedia_setpresentduration","dxgi1_3/IDXGISwapChainMedia::SetPresentDuration"]
old-location: direct3ddxgi\idxgiswapchainmedia_setpresentduration.htm
tech.root: direct3ddxgi
ms.assetid: F2852200-01B4-4CB7-8635-87CF827E1D27
ms.date: 12/05/2018
ms.keywords: IDXGISwapChainMedia interface [DXGI],SetPresentDuration method, IDXGISwapChainMedia.SetPresentDuration, IDXGISwapChainMedia::SetPresentDuration, SetPresentDuration, SetPresentDuration method [DXGI], SetPresentDuration method [DXGI],IDXGISwapChainMedia interface, direct3ddxgi.idxgiswapchainmedia_setpresentduration, dxgi1_3/IDXGISwapChainMedia::SetPresentDuration
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChainMedia::SetPresentDuration
 - dxgi1_3/IDXGISwapChainMedia::SetPresentDuration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChainMedia.SetPresentDuration
---

# IDXGISwapChainMedia::SetPresentDuration


## -description

Requests a custom presentation duration (custom refresh rate).

## -parameters

### -param Duration

The custom presentation duration, specified in hundreds of nanoseconds.

## -returns

This method returns S_OK on success, or a DXGI error code on failure.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia">IDXGISwapChainMedia</a>