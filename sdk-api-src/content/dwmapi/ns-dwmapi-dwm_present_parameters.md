---
UID: NS:dwmapi._DWM_PRESENT_PARAMETERS
title: DWM_PRESENT_PARAMETERS (dwmapi.h)
description: Specifies Desktop Window Manager (DWM) video frame parameters for frame composition. Used by the DwmSetPresentParameters function.
helpviewer_keywords: ["DWM_PRESENT_PARAMETERS","DWM_PRESENT_PARAMETERS structure [Desktop Window Manager]","_udwm_dwm_present_parameters","_udwm_dwm_present_parameters_cpp","dwm.dwm_present_parameters","dwmapi/DWM_PRESENT_PARAMETERS","winui._udwm_dwm_present_parameters"]
old-location: dwm\dwm_present_parameters.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_present_parameters.htm
ms.date: 12/05/2018
ms.keywords: DWM_PRESENT_PARAMETERS, DWM_PRESENT_PARAMETERS structure [Desktop Window Manager], _udwm_dwm_present_parameters, _udwm_dwm_present_parameters_cpp, dwm.dwm_present_parameters, dwmapi/DWM_PRESENT_PARAMETERS, winui._udwm_dwm_present_parameters
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
req.typenames: DWM_PRESENT_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DWM_PRESENT_PARAMETERS
 - dwmapi/_DWM_PRESENT_PARAMETERS
 - DWM_PRESENT_PARAMETERS
 - dwmapi/DWM_PRESENT_PARAMETERS
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
 - DWM_PRESENT_PARAMETERS
---

# DWM_PRESENT_PARAMETERS structure


## -description

Specifies Desktop Window Manager (DWM) video frame parameters for frame composition. Used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetpresentparameters">DwmSetPresentParameters</a> function.

## -struct-fields

### -field cbSize

The size of the <b>DWM_PRESENT_PARAMETERS</b> structure.

### -field fQueue

<b>TRUE</b> if the caller is requesting queued presents; otherwise, <b>FALSE</b>. If <b>TRUE</b>, the remaining parameters must be specified. If <b>FALSE</b>, queued presentation is disabled for this window and present behavior returns to the default behavior.

### -field cRefreshStart

A <b>ULONGLONG</b> value that provides the refresh number that the next presented frame should begin to display.

### -field cBuffer

The number of frames the application is instructing DWM to queue. The valid range is 2-8.

### -field fUseSourceRate

<b>TRUE</b> if the application wants DWM to schedule presentation based on source rate. <b>FALSE</b> if the application will decide how many refreshes to display for each frame. If <b>TRUE</b>, <b>rateSource</b> must be specified. If <b>FALSE</b>, <b>cRefreshesPerFrame</b> must be specified.

### -field rateSource

The rate, in frames per second, of the source material being displayed.

### -field cRefreshesPerFrame

The number of monitor refreshes through which each frame should be displayed on the screen.

### -field eSampling

The frame sampling type to use for composition.

## -remarks

The <b>rateSource</b> member is expressed as a ratio so that content (like that using NTSC standards, which has a rate of 60000/1001) can be accurately expressed. DWM determines how long to display each frame by resampling between the source rate and the composition rate in use each time the desktop is composed.