---
UID: NF:dwmapi.DwmGetCompositionTimingInfo
title: DwmGetCompositionTimingInfo function (dwmapi.h)
description: Retrieves the current composition timing information for a specified window.
helpviewer_keywords: ["DwmGetCompositionTimingInfo","DwmGetCompositionTimingInfo function [Desktop Window Manager]","_udwm_dwmgetcompositiontiminginfo","_udwm_dwmgetcompositiontiminginfo_cpp","dwm.dwmgetcompositiontiminginfo","dwmapi/DwmGetCompositionTimingInfo","winui._udwm_dwmgetcompositiontiminginfo"]
old-location: dwm\dwmgetcompositiontiminginfo.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgetcompositiontiminginfo.htm
ms.date: 12/05/2018
ms.keywords: DwmGetCompositionTimingInfo, DwmGetCompositionTimingInfo function [Desktop Window Manager], _udwm_dwmgetcompositiontiminginfo, _udwm_dwmgetcompositiontiminginfo_cpp, dwm.dwmgetcompositiontiminginfo, dwmapi/DwmGetCompositionTimingInfo, winui._udwm_dwmgetcompositiontiminginfo
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
 - DwmGetCompositionTimingInfo
 - dwmapi/DwmGetCompositionTimingInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - API-MS-Win-dwmapi-l1-1-0.dll
 - Ext-Ms-Win-DwmAPI-Ext-L1-1-0.dll
api_name:
 - DwmGetCompositionTimingInfo
---

# DwmGetCompositionTimingInfo function


## -description

Retrieves the current composition timing information for a specified window.

## -parameters

### -param hwnd [in]

The handle to the window for which the composition timing information should be retrieved.

Starting with Windows 8.1, this parameter must be set to <b>NULL</b>. If this parameter is not set to <b>NULL</b>, <b>DwmGetCompositionTimingInfo</b> returns E_INVALIDARG.

### -param pTimingInfo [out]

A pointer to a <a href="/windows/desktop/api/dwmapi/ns-dwmapi-dwm_timing_info">DWM_TIMING_INFO</a> structure that, when this function returns successfully, receives the current composition timing information for the window. The <b>cbSize</b> member of this structure must be set before this function is called.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.