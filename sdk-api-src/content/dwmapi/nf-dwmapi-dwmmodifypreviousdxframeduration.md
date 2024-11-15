---
UID: NF:dwmapi.DwmModifyPreviousDxFrameDuration
title: DwmModifyPreviousDxFrameDuration function (dwmapi.h)
description: Changes the number of monitor refreshes through which the previous frame will be displayed. DwmModifyPreviousDxFrameDuration is no longer supported. Starting with Windows 8.1, calls to DwmModifyPreviousDxFrameDuration always return E_NOTIMPL.
helpviewer_keywords: ["DwmModifyPreviousDxFrameDuration","DwmModifyPreviousDxFrameDuration function [Desktop Window Manager]","_udwm_dwmmodifypreviousdxframeduration","_udwm_dwmmodifypreviousdxframeduration_cpp","dwm.dwmmodifypreviousdxframeduration","dwmapi/DwmModifyPreviousDxFrameDuration","winui._udwm_dwmmodifypreviousdxframeduration"]
old-location: dwm\dwmmodifypreviousdxframeduration.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmmodifypreviousdxframeduration.htm
ms.date: 12/05/2018
ms.keywords: DwmModifyPreviousDxFrameDuration, DwmModifyPreviousDxFrameDuration function [Desktop Window Manager], _udwm_dwmmodifypreviousdxframeduration, _udwm_dwmmodifypreviousdxframeduration_cpp, dwm.dwmmodifypreviousdxframeduration, dwmapi/DwmModifyPreviousDxFrameDuration, winui._udwm_dwmmodifypreviousdxframeduration
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
 - DwmModifyPreviousDxFrameDuration
 - dwmapi/DwmModifyPreviousDxFrameDuration
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
 - DwmModifyPreviousDxFrameDuration
---

# DwmModifyPreviousDxFrameDuration function


## -description

Changes the number of monitor refreshes through which the previous frame will be displayed.
        
            

<b>DwmModifyPreviousDxFrameDuration</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmModifyPreviousDxFrameDuration</b> always return E_NOTIMPL.

## -parameters

### -param hwnd [in]

The handle to the window for which the new duration is applied to the previous frame.

### -param cRefreshes [in]

The number of refreshes to apply to the previous frame.

### -param fRelative [in]

<b>TRUE</b> if the value given in <i>cRefreshes</i> is relative to the current value (added to or subtracted from it); <b>FALSE</b> if the value replaces the current value.

## -returns

This function always returns S_OK, even when DWM is not running.

