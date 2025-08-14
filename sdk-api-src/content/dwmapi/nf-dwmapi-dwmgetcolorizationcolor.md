---
UID: NF:dwmapi.DwmGetColorizationColor
title: DwmGetColorizationColor function (dwmapi.h)
description: Retrieves the current color used for Desktop Window Manager (DWM) glass composition.
helpviewer_keywords: ["DwmGetColorizationColor","DwmGetColorizationColor function [Desktop Window Manager]","_udwm_dwmgetcolorizationcolor","_udwm_dwmgetcolorizationcolor_cpp","dwm.dwmgetcolorizationcolor","dwmapi/DwmGetColorizationColor","winui._udwm_dwmgetcolorizationcolor"]
old-location: dwm\dwmgetcolorizationcolor.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgetcolorizationcolor.htm
ms.date: 12/05/2018
ms.keywords: DwmGetColorizationColor, DwmGetColorizationColor function [Desktop Window Manager], _udwm_dwmgetcolorizationcolor, _udwm_dwmgetcolorizationcolor_cpp, dwm.dwmgetcolorizationcolor, dwmapi/DwmGetColorizationColor, winui._udwm_dwmgetcolorizationcolor
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
 - DwmGetColorizationColor
 - dwmapi/DwmGetColorizationColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
api_name:
 - DwmGetColorizationColor
---

# DwmGetColorizationColor function


## -description

Retrieves the current color used for Desktop Window Manager (DWM) glass composition. This value is based on the current color scheme and can be modified by the user. Applications can listen for color changes by handling the <a href="/windows/desktop/dwm/wm-dwmcolorizationcolorchanged">WM_DWMCOLORIZATIONCOLORCHANGED</a> notification.

## -parameters

### -param pcrColorization [out]

A pointer to a value that, when this function returns successfully, receives the current color used for glass composition. The color format of the value is 0xAARRGGBB.

### -param pfOpaqueBlend [out]

A pointer to a value that, when this function returns successfully, indicates whether the color is an opaque blend. <b>TRUE</b> if the color is an opaque blend; otherwise, <b>FALSE</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value pointed to by <i>pcrColorization</i> is in an 0xAARRGGBB format. Many Microsoft Win32 APIs, such as <a href="/windows/desktop/gdi/colorref">COLORREF</a>, use a 0x00BBGGRR format. Be careful to assure that the intended colors are used.


#### Examples

The following example code shows a <a href="/windows/desktop/dwm/wm-dwmcolorizationcolorchanged">WM_DWMCOLORIZATIONCOLORCHANGED</a> notification handle. If the colorization notification is received, this code retrieves the new color value.


```cpp

...
DWORD color = 0;
BOOL opaque = FALSE;
  
HRESULT hr = DwmGetColorizationColor(&color, &opaque);
if (SUCCEEDED(hr))
{
  // Update the application to use the new color.
}
...
```