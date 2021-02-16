---
UID: NS:dwmapi._DWM_BLURBEHIND
title: DWM_BLURBEHIND (dwmapi.h)
description: Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the DwmEnableBlurBehindWindow function.
helpviewer_keywords: ["*PDWM_BLURBEHIND","DWM_BLURBEHIND","DWM_BLURBEHIND structure [Desktop Window Manager]","PDWM_BLURBEHIND","PDWM_BLURBEHIND structure pointer [Desktop Window Manager]","_udwm_dwm_blurbehind","_udwm_dwm_blurbehind_cpp","dwm.dwm_blurbehind","dwmapi/DWM_BLURBEHIND","dwmapi/PDWM_BLURBEHIND","winui._udwm_dwm_blurbehind"]
old-location: dwm\dwm_blurbehind.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_blurbehind.htm
ms.date: 12/05/2018
ms.keywords: '*PDWM_BLURBEHIND, DWM_BLURBEHIND, DWM_BLURBEHIND structure [Desktop Window Manager], PDWM_BLURBEHIND, PDWM_BLURBEHIND structure pointer [Desktop Window Manager], _udwm_dwm_blurbehind, _udwm_dwm_blurbehind_cpp, dwm.dwm_blurbehind, dwmapi/DWM_BLURBEHIND, dwmapi/PDWM_BLURBEHIND, winui._udwm_dwm_blurbehind'
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
req.typenames: DWM_BLURBEHIND, *PDWM_BLURBEHIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DWM_BLURBEHIND
 - dwmapi/_DWM_BLURBEHIND
 - PDWM_BLURBEHIND
 - dwmapi/PDWM_BLURBEHIND
 - DWM_BLURBEHIND
 - dwmapi/DWM_BLURBEHIND
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
 - DWM_BLURBEHIND
---

# DWM_BLURBEHIND structure


## -description

Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow">DwmEnableBlurBehindWindow</a> function.

## -struct-fields

### -field dwFlags

A bitwise combination of <a href="/windows/desktop/dwm/dwm-bb-constants">DWM Blur Behind</a> constant values that indicates which of the members of this structure have been set.

### -field fEnable

<b>TRUE</b> to register the window handle to DWM blur behind; <b>FALSE</b> to unregister the window handle from DWM blur behind.

### -field hRgnBlur

The region within the client area where the blur behind will be applied. A <b>NULL</b> value will apply the blur behind the entire client area.

### -field fTransitionOnMaximized

<b>TRUE</b> if the window's colorization should transition to match the maximized windows; otherwise, <b>FALSE</b>.