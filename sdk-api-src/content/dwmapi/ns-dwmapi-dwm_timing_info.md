---
UID: NS:dwmapi._DWM_TIMING_INFO
title: DWM_TIMING_INFO (dwmapi.h)
description: Specifies Desktop Window Manager (DWM) composition timing information. Used by the DwmGetCompositionTimingInfo function.
helpviewer_keywords: ["DWM_TIMING_INFO","DWM_TIMING_INFO structure [Desktop Window Manager]","_udwm_dwm_timing_info","_udwm_dwm_timing_info_cpp","dwm.dwm_timing_info","dwmapi/DWM_TIMING_INFO","winui._udwm_dwm_timing_info"]
old-location: dwm\dwm_timing_info.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_timing_info.htm
ms.date: 12/05/2018
ms.keywords: DWM_TIMING_INFO, DWM_TIMING_INFO structure [Desktop Window Manager], _udwm_dwm_timing_info, _udwm_dwm_timing_info_cpp, dwm.dwm_timing_info, dwmapi/DWM_TIMING_INFO, winui._udwm_dwm_timing_info
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DWM_TIMING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DWM_TIMING_INFO
 - dwmapi/_DWM_TIMING_INFO
 - DWM_TIMING_INFO
 - dwmapi/DWM_TIMING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWM_TIMING_INFO
---

# DWM_TIMING_INFO structure


## -description

Specifies Desktop Window Manager (DWM) composition timing information. Used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo">DwmGetCompositionTimingInfo</a> function.

## -struct-fields

### -field cbSize

The size of this <b>DWM_TIMING_INFO</b> structure.

### -field rateRefresh

The monitor refresh rate.

### -field qpcRefreshPeriod

The monitor refresh period.

### -field rateCompose

The composition rate.

### -field qpcVBlank

The query performance counter value before the vertical blank.

### -field cRefresh

The DWM refresh counter.

### -field cDXRefresh

The DirectX refresh counter.

### -field qpcCompose

The query performance counter value for a frame composition.

### -field cFrame

The frame number that was composed at <b>qpcCompose</b>.

### -field cDXPresent

The DirectX present number used to identify rendering frames.

### -field cRefreshFrame

The refresh count of the frame that was composed at <b>qpcCompose</b>.

### -field cFrameSubmitted

The DWM frame number that was last submitted.

### -field cDXPresentSubmitted

The DirectX present number that was last submitted.

### -field cFrameConfirmed

The DWM frame number that was last confirmed as presented.

### -field cDXPresentConfirmed

The DirectX present number that was last confirmed as presented.

### -field cRefreshConfirmed

The target refresh count of the last frame confirmed as completed by the GPU.

### -field cDXRefreshConfirmed

The DirectX refresh count when the frame was confirmed as presented.

### -field cFramesLate

The number of frames the DWM presented late.

### -field cFramesOutstanding

The number of composition frames that have been issued but have not been confirmed as completed.

### -field cFrameDisplayed

The last frame displayed.

### -field qpcFrameDisplayed

The QPC time of the composition pass when the frame was displayed.

### -field cRefreshFrameDisplayed

The vertical refresh count when the frame should have become visible.

### -field cFrameComplete

The ID of the last frame marked as completed.

### -field qpcFrameComplete

The QPC time when the last frame was marked as completed.

### -field cFramePending

The ID of the last frame marked as pending.

### -field qpcFramePending

The QPC time when the last frame was marked as pending.

### -field cFramesDisplayed

The number of unique frames displayed. This value is valid only after a second call to the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo">DwmGetCompositionTimingInfo</a> function.

### -field cFramesComplete

The number of new completed frames that have been received.

### -field cFramesPending

The number of new frames submitted to DirectX but not yet completed.

### -field cFramesAvailable

The number of frames available but not displayed, used, or dropped. This value is valid only after a second call to <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo">DwmGetCompositionTimingInfo</a>.

### -field cFramesDropped

The number of rendered frames that were never displayed because composition occurred too late. This value is valid only after a second call to <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo">DwmGetCompositionTimingInfo</a>.

### -field cFramesMissed

The number of times an old frame was composed when a new frame should have been used but was not available.

### -field cRefreshNextDisplayed

The frame count at which the next frame is scheduled to be displayed.

### -field cRefreshNextPresented

The frame count at which the next DirectX present is scheduled to be displayed.

### -field cRefreshesDisplayed

The total number of refreshes that have been displayed for the application since the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetpresentparameters">DwmSetPresentParameters</a> function was last called.

### -field cRefreshesPresented

The total number of refreshes that have been presented by the application since <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetpresentparameters">DwmSetPresentParameters</a> was last called.

### -field cRefreshStarted

The refresh number when content for this window started to be displayed.

### -field cPixelsReceived

The total number of pixels DirectX redirected to the DWM.

### -field cPixelsDrawn

The number of pixels drawn.

### -field cBuffersEmpty

The number of empty buffers in the flip chain.

## -remarks

Both DWM_FRAME_COUNT and QPC_TIME are defined in Dwmapi.h as <b>ULONGLONG</b>.