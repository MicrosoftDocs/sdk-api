---
UID: NF:dwmapi.DwmSetDxFrameDuration
title: DwmSetDxFrameDuration function (dwmapi.h)
description: Sets the number of monitor refreshes through which to display the presented frame. DwmSetDxFrameDuration is no longer supported. Starting with Windows 8.1, calls to DwmSetDxFrameDuration always return E_NOTIMPL.
helpviewer_keywords: ["DwmSetDxFrameDuration","DwmSetDxFrameDuration function [Desktop Window Manager]","_udwm_dwmsetdxframeduration","_udwm_dwmsetdxframeduration_cpp","dwm.dwmsetdxframeduration","dwmapi/DwmSetDxFrameDuration","winui._udwm_dwmsetdxframeduration"]
old-location: dwm\dwmsetdxframeduration.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmsetdxframeduration.htm
ms.date: 12/05/2018
ms.keywords: DwmSetDxFrameDuration, DwmSetDxFrameDuration function [Desktop Window Manager], _udwm_dwmsetdxframeduration, _udwm_dwmsetdxframeduration_cpp, dwm.dwmsetdxframeduration, dwmapi/DwmSetDxFrameDuration, winui._udwm_dwmsetdxframeduration
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
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmSetDxFrameDuration
 - dwmapi/DwmSetDxFrameDuration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmSetDxFrameDuration
---

# DwmSetDxFrameDuration function


## -description

Sets the number of monitor refreshes through which to display the presented frame.
        
            

<b>DwmSetDxFrameDuration</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmSetDxFrameDuration</b> always return E_NOTIMPL.

## -parameters

### -param hwnd [in]

The handle to the window that displays the presented frame.

### -param cRefreshes [in]

The number of refreshes through which to display the presented frame.

## -returns

This function always returns S_OK, even when the frame duration is not changed or DWM is not running.

## -remarks

The DWM will attempt to display the presented frame for at least the number of monitor refreshes specified. It might be impossible to display the frame for the precise number of refreshes due to the current composition rate. If the frame is presented late to the DWM or the DWM is late in composing, a frame could be displayed for fewer than the number of refreshes requested or even skipped completely.

