---
UID: NS:dxgi1_3.DXGI_FRAME_STATISTICS_MEDIA
title: DXGI_FRAME_STATISTICS_MEDIA (dxgi1_3.h)
description: Used to verify system approval for the app's custom present duration (custom refresh rate).
helpviewer_keywords: ["DXGI_FRAME_STATISTICS_MEDIA","DXGI_FRAME_STATISTICS_MEDIA structure [DXGI]","direct3ddxgi.dxgi_frame_statistics_media","dxgi1_3/DXGI_FRAME_STATISTICS_MEDIA"]
old-location: direct3ddxgi\dxgi_frame_statistics_media.htm
tech.root: direct3ddxgi
ms.assetid: BC23B5C1-8257-4556-B930-E09FE60D536C
ms.date: 12/05/2018
ms.keywords: DXGI_FRAME_STATISTICS_MEDIA, DXGI_FRAME_STATISTICS_MEDIA structure [DXGI], direct3ddxgi.dxgi_frame_statistics_media, dxgi1_3/DXGI_FRAME_STATISTICS_MEDIA
req.header: dxgi1_3.h
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
req.typenames: DXGI_FRAME_STATISTICS_MEDIA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_FRAME_STATISTICS_MEDIA
 - dxgi1_3/DXGI_FRAME_STATISTICS_MEDIA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_FRAME_STATISTICS_MEDIA
---

# DXGI_FRAME_STATISTICS_MEDIA structure


## -description

Used to verify system approval for the app's custom present duration (custom refresh rate). Approval should be continuously verified on a frame-by-frame basis.

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

### -field CompositionMode

Type: <b><a href="/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode">DXGI_FRAME_PRESENTATION_MODE</a></b>

A value indicating the composition presentation mode. This value is used to determine whether the app should continue to use the decode swap chain. See <a href="/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode">DXGI_FRAME_PRESENTATION_MODE</a>.

### -field ApprovedPresentDuration

Type: <b>UINT</b>

If the system approves an app's custom present duration request, this field is set to the approved custom present duration.

If the app's custom present duration request is not approved, this field is set to zero.

## -remarks

This structure is used with the <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchainmedia-getframestatisticsmedia">GetFrameStatisticsMedia</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia">IDXGISwapChainMedia</a>