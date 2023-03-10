---
UID: NF:dxgi.IDXGIOutput.GetFrameStatistics
title: IDXGIOutput::GetFrameStatistics (dxgi.h)
description: Gets statistics about recently rendered frames.
helpviewer_keywords: ["2986a9cc-4b09-8622-8d30-17f06409df3a","GetFrameStatistics","GetFrameStatistics method [DXGI]","GetFrameStatistics method [DXGI]","IDXGIOutput interface","IDXGIOutput interface [DXGI]","GetFrameStatistics method","IDXGIOutput.GetFrameStatistics","IDXGIOutput::GetFrameStatistics","direct3ddxgi.idxgioutput_getframestatistics","dxgi/IDXGIOutput::GetFrameStatistics"]
old-location: direct3ddxgi\idxgioutput_getframestatistics.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getframestatistics.htm
ms.date: 12/05/2018
ms.keywords: 2986a9cc-4b09-8622-8d30-17f06409df3a, GetFrameStatistics, GetFrameStatistics method [DXGI], GetFrameStatistics method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetFrameStatistics method, IDXGIOutput.GetFrameStatistics, IDXGIOutput::GetFrameStatistics, direct3ddxgi.idxgioutput_getframestatistics, dxgi/IDXGIOutput::GetFrameStatistics
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput::GetFrameStatistics
 - dxgi/IDXGIOutput::GetFrameStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput.GetFrameStatistics
---

# IDXGIOutput::GetFrameStatistics


## -description

Gets statistics about recently rendered frames.

## -parameters

### -param pStats [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_frame_statistics">DXGI_FRAME_STATISTICS</a>*</b>

A pointer to frame statistics (see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_frame_statistics">DXGI_FRAME_STATISTICS</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns S_OK. Otherwise, it might return <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>.

## -remarks

This API is similar to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getframestatistics">IDXGISwapChain::GetFrameStatistics</a>.


<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>