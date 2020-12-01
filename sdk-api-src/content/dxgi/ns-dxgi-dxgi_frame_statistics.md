---
UID: NS:dxgi.DXGI_FRAME_STATISTICS
title: DXGI_FRAME_STATISTICS (dxgi.h)
description: Describes timing and presentation statistics for a frame.
helpviewer_keywords: ["97415a25-57a3-0530-e47d-4459bac66c73","DXGI_FRAME_STATISTICS","DXGI_FRAME_STATISTICS structure [DXGI]","direct3ddxgi.dxgi_frame_statistics","dxgi/DXGI_FRAME_STATISTICS"]
old-location: direct3ddxgi\dxgi_frame_statistics.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_frame_statistics.htm
ms.date: 12/05/2018
ms.keywords: 97415a25-57a3-0530-e47d-4459bac66c73, DXGI_FRAME_STATISTICS, DXGI_FRAME_STATISTICS structure [DXGI], direct3ddxgi.dxgi_frame_statistics, dxgi/DXGI_FRAME_STATISTICS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_FRAME_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_FRAME_STATISTICS
 - dxgi/DXGI_FRAME_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_FRAME_STATISTICS
---

# DXGI_FRAME_STATISTICS structure


## -description

Describes timing and presentation statistics for a frame.

## -struct-fields

### -field PresentCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that represents the running total count of times that an image was presented to the monitor since the computer booted.

<div class="alert"><b>Note</b>  The number of times that an image was presented to the monitor is not necessarily the same as the number of times 
        that you called <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>.</div>
<div> </div>

### -field PresentRefreshCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that represents  the running total count of v-blanks at which the last image was presented to the monitor and that have happened since the computer booted (for windowed mode, since the swap chain was created).

### -field SyncRefreshCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that represents  the running total count of v-blanks when the scheduler last sampled the machine time by calling <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> and that have happened since the computer booted (for windowed mode, since the swap chain was created).

### -field SyncQPCTime

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

A value that represents the high-resolution performance counter timer. 
        This value is the same as the value returned by the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> 
        function.

### -field SyncGPUTime

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

Reserved. Always returns 0.

## -remarks

You initialize the <b>DXGI_FRAME_STATISTICS</b> structure with the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getframestatistics">IDXGIOutput::GetFrameStatistics</a> or <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getframestatistics">IDXGISwapChain::GetFrameStatistics</a> method.

You can only use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getframestatistics">IDXGISwapChain::GetFrameStatistics</a> for swap chains that either use the flip presentation model or draw in full-screen mode. You set the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure to specify that the swap chain uses the flip presentation model.

The values in the <b>PresentCount</b> and <b>PresentRefreshCount</b> members indicate information about when a frame was presented on the display screen. You can use these values to determine whether a glitch occurred. The values in the <b>SyncRefreshCount</b> and <b>SyncQPCTime</b> members indicate timing information that you can use for audio and video synchronization or very precise animation. If the swap chain draws in full-screen mode, these values are based on when the computer booted. 
If the swap chain draws in windowed mode, these values are based on when the swap chain is created.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>