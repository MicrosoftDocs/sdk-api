---
UID: NN:dxgi1_3.IDXGISwapChainMedia
title: IDXGISwapChainMedia (dxgi1_3.h)
description: This swap chain interface allows desktop media applications to request a seamless change to a specific refresh rate.
helpviewer_keywords: ["IDXGISwapChainMedia","IDXGISwapChainMedia interface [DXGI]","IDXGISwapChainMedia interface [DXGI]","described","direct3ddxgi.idxgiswapchainmedia","dxgi1_3/IDXGISwapChainMedia"]
old-location: direct3ddxgi\idxgiswapchainmedia.htm
tech.root: direct3ddxgi
ms.assetid: 80C2A6D8-3435-4671-A473-0EF0F5A70ADB
ms.date: 12/05/2018
ms.keywords: IDXGISwapChainMedia, IDXGISwapChainMedia interface [DXGI], IDXGISwapChainMedia interface [DXGI],described, direct3ddxgi.idxgiswapchainmedia, dxgi1_3/IDXGISwapChainMedia
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
 - IDXGISwapChainMedia
 - dxgi1_3/IDXGISwapChainMedia
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
 - IDXGISwapChainMedia
---

# IDXGISwapChainMedia interface


## -description

This swap chain interface allows desktop media applications to request a seamless change to a specific refresh rate.

For example, a media application presenting video at a typical framerate of 23.997 frames per second can request a custom refresh rate of 24 or 48 Hz to eliminate jitter. If the request is approved, the app starts presenting frames at the custom refresh rate immediately - without the typical 'mode switch' a user would experience when changing the refresh rate themselves by using the control panel.

## -inheritance

The <b>IDXGISwapChainMedia</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGISwapChainMedia</b> also has these types of members:

## -remarks

Seamless changes to custom framerates can only be done on integrated panels. Custom frame rates cannot be applied to external displays. If the DXGI output adapter is attached to an external display then <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchainmedia-checkpresentdurationsupport">CheckPresentDurationSupport</a> will return (0, 0) for upper and lower bounds, indicating that the device does not support seamless refresh rate changes.
        

Custom refresh rates can be used when displaying video with a dynamic framerate. However, the refresh rate change should be kept imperceptible to the user. A best practice for keeping the refresh rate transition imperceptible  is to only set the custom framerate if the app determines it can present at that rate for least 5 seconds.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactorymedia">IDXGIFactoryMedia</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
