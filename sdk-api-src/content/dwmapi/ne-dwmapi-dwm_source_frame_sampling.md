---
UID: NE:dwmapi.DWM_SOURCE_FRAME_SAMPLING
title: DWM_SOURCE_FRAME_SAMPLING (dwmapi.h)
description: Flags used by the DwmSetPresentParameters function to specify the frame sampling type.
helpviewer_keywords: ["DWM_SOURCE_FRAME_SAMPLING","DWM_SOURCE_FRAME_SAMPLING enumeration [Desktop Window Manager]","DWM_SOURCE_FRAME_SAMPLING_COVERAGE","DWM_SOURCE_FRAME_SAMPLING_LAST","DWM_SOURCE_FRAME_SAMPLING_POINT","_udwm_dwm_source_frame_sampling","_udwm_dwm_source_frame_sampling_cpp","dwm.dwm_source_frame_sampling","dwmapi/DWM_SOURCE_FRAME_SAMPLING","dwmapi/DWM_SOURCE_FRAME_SAMPLING_COVERAGE","dwmapi/DWM_SOURCE_FRAME_SAMPLING_LAST","dwmapi/DWM_SOURCE_FRAME_SAMPLING_POINT","winui._udwm_dwm_source_frame_sampling"]
old-location: dwm\dwm_source_frame_sampling.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\enums\dwm_source_frame_sampling.htm
ms.date: 12/05/2018
ms.keywords: DWM_SOURCE_FRAME_SAMPLING, DWM_SOURCE_FRAME_SAMPLING enumeration [Desktop Window Manager], DWM_SOURCE_FRAME_SAMPLING_COVERAGE, DWM_SOURCE_FRAME_SAMPLING_LAST, DWM_SOURCE_FRAME_SAMPLING_POINT, _udwm_dwm_source_frame_sampling, _udwm_dwm_source_frame_sampling_cpp, dwm.dwm_source_frame_sampling, dwmapi/DWM_SOURCE_FRAME_SAMPLING, dwmapi/DWM_SOURCE_FRAME_SAMPLING_COVERAGE, dwmapi/DWM_SOURCE_FRAME_SAMPLING_LAST, dwmapi/DWM_SOURCE_FRAME_SAMPLING_POINT, winui._udwm_dwm_source_frame_sampling
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
req.typenames: DWM_SOURCE_FRAME_SAMPLING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWM_SOURCE_FRAME_SAMPLING
 - dwmapi/DWM_SOURCE_FRAME_SAMPLING
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
 - DWM_SOURCE_FRAME_SAMPLING
---

# DWM_SOURCE_FRAME_SAMPLING enumeration


## -description

Flags used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetpresentparameters">DwmSetPresentParameters</a> function to specify the frame sampling type.

## -enum-fields

### -field DWM_SOURCE_FRAME_SAMPLING_POINT

Use the first source frame that includes the first refresh of the output frame.

### -field DWM_SOURCE_FRAME_SAMPLING_COVERAGE

Use the source frame that includes the most refreshes of the output frame. In the case of multiple source frames with the same coverage, the last frame is used.

### -field DWM_SOURCE_FRAME_SAMPLING_LAST

The maximum recognized <a href="/windows/desktop/api/dwmapi/ne-dwmapi-dwm_source_frame_sampling">DWM_SOURCE_FRAME_SAMPLING</a> value, used for validation purposes.

