---
UID: NF:mfmediaengine.IMFMediaEngineEx.EnableWindowlessSwapchainMode
title: IMFMediaEngineEx::EnableWindowlessSwapchainMode (mfmediaengine.h)
description: Enables or disables windowless swap-chain mode.
helpviewer_keywords: ["EnableWindowlessSwapchainMode","EnableWindowlessSwapchainMode method [Media Foundation]","EnableWindowlessSwapchainMode method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","EnableWindowlessSwapchainMode method","IMFMediaEngineEx.EnableWindowlessSwapchainMode","IMFMediaEngineEx::EnableWindowlessSwapchainMode","mf.imfmediaengineex_enablewindowlessswapchainmode","mfmediaengine/IMFMediaEngineEx::EnableWindowlessSwapchainMode"]
old-location: mf\imfmediaengineex_enablewindowlessswapchainmode.htm
tech.root: mf
ms.assetid: B93429D7-A0DF-4440-A164-C140334FC0A6
ms.date: 12/05/2018
ms.keywords: EnableWindowlessSwapchainMode, EnableWindowlessSwapchainMode method [Media Foundation], EnableWindowlessSwapchainMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],EnableWindowlessSwapchainMode method, IMFMediaEngineEx.EnableWindowlessSwapchainMode, IMFMediaEngineEx::EnableWindowlessSwapchainMode, mf.imfmediaengineex_enablewindowlessswapchainmode, mfmediaengine/IMFMediaEngineEx::EnableWindowlessSwapchainMode
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
 - IMFMediaEngineEx::EnableWindowlessSwapchainMode
 - mfmediaengine/IMFMediaEngineEx::EnableWindowlessSwapchainMode
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
 - IMFMediaEngineEx.EnableWindowlessSwapchainMode
---

# IMFMediaEngineEx::EnableWindowlessSwapchainMode


## -description

Enables or disables windowless swap-chain mode.

## -parameters

### -param fEnable [in]

If <b>TRUE</b>, windowless swap-chain mode is enabled.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In windowless swap-chain mode, the Media Engine creates a windowless swap chain and presents video frames to the swap chain. To render the video, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getvideoswapchainhandle">IMFMediaEngineEx::GetVideoSwapchainHandle</a> to get a handle to the swap chain, and then associate the handle with a Microsoft DirectComposition visual.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>