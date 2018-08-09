---
UID: NF:dwmapi.DwmModifyPreviousDxFrameDuration
title: DwmModifyPreviousDxFrameDuration function
author: windows-sdk-content
description: Changes the number of monitor refreshes through which the previous frame will be displayed. DwmModifyPreviousDxFrameDuration is no longer supported. Starting with Windows 8.1, calls to DwmModifyPreviousDxFrameDuration always return E_NOTIMPL.
old-location: dwm\dwmmodifypreviousdxframeduration.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmmodifypreviousdxframeduration.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmModifyPreviousDxFrameDuration, DwmModifyPreviousDxFrameDuration function [Desktop Window Manager], _udwm_dwmmodifypreviousdxframeduration, _udwm_dwmmodifypreviousdxframeduration_cpp, dwm.dwmmodifypreviousdxframeduration, dwmapi/DwmModifyPreviousDxFrameDuration, winui._udwm_dwmmodifypreviousdxframeduration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmModifyPreviousDxFrameDuration
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmModifyPreviousDxFrameDuration function


## -description


Changes the number of monitor refreshes through which the previous frame will be displayed.
        
            

<b>DwmModifyPreviousDxFrameDuration</b> is no longer supported. Starting with Windows 8.1, calls to <b>DwmModifyPreviousDxFrameDuration</b> always return E_NOTIMPL.


## -parameters




### -param hwnd

The handle to the window for which the new duration is applied to the previous frame.


### -param cRefreshes

The number of refreshes to apply to the previous frame.


### -param fRelative

<b>TRUE</b> if the value given in <i>cRefreshes</i> is relative to the current value (added to or subtracted from it); <b>FALSE</b> if the value replaces the current value.


## -returns



This function always returns S_OK, even when DWM is not running.



