---
UID: NF:dwmapi.DwmInvalidateIconicBitmaps
title: DwmInvalidateIconicBitmaps function (dwmapi.h)
description: Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.
helpviewer_keywords: ["DwmInvalidateIconicBitmaps","DwmInvalidateIconicBitmaps function [Desktop Window Manager]","_udwm_dwminvalidateiconicbitmaps","_udwm_dwminvalidateiconicbitmaps_cpp","dwm.dwminvalidateiconicbitmaps","dwmapi/DwmInvalidateIconicBitmaps","winui._udwm_dwminvalidateiconicbitmaps"]
old-location: dwm\dwminvalidateiconicbitmaps.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwminvalidateiconicbitmaps.htm
ms.date: 12/05/2018
ms.keywords: DwmInvalidateIconicBitmaps, DwmInvalidateIconicBitmaps function [Desktop Window Manager], _udwm_dwminvalidateiconicbitmaps, _udwm_dwminvalidateiconicbitmaps_cpp, dwm.dwminvalidateiconicbitmaps, dwmapi/DwmInvalidateIconicBitmaps, winui._udwm_dwminvalidateiconicbitmaps
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Dwmapi.dll; Uxtheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmInvalidateIconicBitmaps
 - dwmapi/DwmInvalidateIconicBitmaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - uxtheme.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
api_name:
 - DwmInvalidateIconicBitmaps
---

# DwmInvalidateIconicBitmaps function


## -description

Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.

## -parameters

### -param hwnd [in]

A handle to the window or tab whose bitmaps are being invalidated through this call. This window must belong to the calling process.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this function causes the Desktop Window Manager (DWM) to invalidate its current bitmaps for the window and request new bitmaps from the window when they are next needed. <b>DwmInvalidateIconicBitmaps</b> should not be called frequently. Doing so can lead to poor performance as new bitmaps are created and retrieved.

