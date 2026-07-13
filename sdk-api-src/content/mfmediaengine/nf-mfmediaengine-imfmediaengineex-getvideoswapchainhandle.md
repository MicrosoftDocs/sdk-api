---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetVideoSwapchainHandle
title: IMFMediaEngineEx::GetVideoSwapchainHandle (mfmediaengine.h)
description: Gets a handle to the windowless swap chain.
helpviewer_keywords: ["GetVideoSwapchainHandle","GetVideoSwapchainHandle method [Media Foundation]","GetVideoSwapchainHandle method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetVideoSwapchainHandle method","IMFMediaEngineEx.GetVideoSwapchainHandle","IMFMediaEngineEx::GetVideoSwapchainHandle","mf.imfmediaengineex_getvideoswapchainhandle","mfmediaengine/IMFMediaEngineEx::GetVideoSwapchainHandle"]
old-location: mf\imfmediaengineex_getvideoswapchainhandle.htm
tech.root: mf
ms.assetid: 23AE2296-F0BF-4060-9849-F6A0E0C13B86
ms.date: 12/05/2018
ms.keywords: GetVideoSwapchainHandle, GetVideoSwapchainHandle method [Media Foundation], GetVideoSwapchainHandle method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetVideoSwapchainHandle method, IMFMediaEngineEx.GetVideoSwapchainHandle, IMFMediaEngineEx::GetVideoSwapchainHandle, mf.imfmediaengineex_getvideoswapchainhandle, mfmediaengine/IMFMediaEngineEx::GetVideoSwapchainHandle
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::GetVideoSwapchainHandle
 - mfmediaengine/IMFMediaEngineEx::GetVideoSwapchainHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetVideoSwapchainHandle
---

# IMFMediaEngineEx::GetVideoSwapchainHandle


## -description

Gets a handle to the windowless swap chain.

## -parameters

### -param phSwapchain [out]

Receives a handle to the swap chain.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To enable windowless swap-chain mode, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-enablewindowlessswapchainmode">IMFMediaEngineEx::EnableWindowlessSwapchainMode</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>