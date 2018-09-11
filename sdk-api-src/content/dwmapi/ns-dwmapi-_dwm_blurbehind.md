---
UID: NS:dwmapi._DWM_BLURBEHIND
title: "_DWM_BLURBEHIND"
author: windows-sdk-content
description: Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the DwmEnableBlurBehindWindow function.
old-location: dwm\dwm_blurbehind.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_blurbehind.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDWM_BLURBEHIND, DWM_BLURBEHIND, DWM_BLURBEHIND structure [Desktop Window Manager], PDWM_BLURBEHIND, PDWM_BLURBEHIND structure pointer [Desktop Window Manager], _DWM_BLURBEHIND, _udwm_dwm_blurbehind, _udwm_dwm_blurbehind_cpp, dwm.dwm_blurbehind, dwmapi/DWM_BLURBEHIND, dwmapi/PDWM_BLURBEHIND, winui._udwm_dwm_blurbehind"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWM_BLURBEHIND
product: Windows
targetos: Windows
req.typenames: DWM_BLURBEHIND, *PDWM_BLURBEHIND
req.redist: 
---

# _DWM_BLURBEHIND structure


## -description


Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the <a href="https://msdn.microsoft.com/en-us/library/Aa969508(v=VS.85).aspx">DwmEnableBlurBehindWindow</a> function.


## -struct-fields




### -field dwFlags

A bitwise combination of <a href="https://msdn.microsoft.com/en-us/library/Aa969533(v=VS.85).aspx">DWM Blur Behind</a> constant values that indicates which of the members of this structure have been set.


### -field fEnable

<b>TRUE</b> to register the window handle to DWM blur behind; <b>FALSE</b> to unregister the window handle from DWM blur behind.


### -field hRgnBlur

The region within the client area where the blur behind will be applied. A <b>NULL</b> value will apply the blur behind the entire client area.


### -field fTransitionOnMaximized

<b>TRUE</b> if the window's colorization should transition to match the maximized windows; otherwise, <b>FALSE</b>.

