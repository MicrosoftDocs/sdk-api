---
UID: NF:uxtheme.OpenThemeDataForDpi
title: OpenThemeDataForDpi function (uxtheme.h)
description: A variant of OpenThemeData that opens a theme handle associated with a specific DPI.
helpviewer_keywords: ["OpenThemeDataForDpi","OpenThemeDataForDpi function [High DPI]","hidpi.openthemedatafordpi","uxtheme/OpenThemeDataForDpi"]
old-location: hidpi\openthemedatafordpi.htm
tech.root: hidpi
ms.assetid: 40044856-82F2-47E2-AD4B-5E4F3868E7B8
ms.date: 12/05/2018
ms.keywords: OpenThemeDataForDpi, OpenThemeDataForDpi function [High DPI], hidpi.openthemedatafordpi, uxtheme/OpenThemeDataForDpi
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: uxtheme.lib
req.dll: uxtheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenThemeDataForDpi
 - uxtheme/OpenThemeDataForDpi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - uxtheme.dll
api_name:
 - OpenThemeDataForDpi
---

# OpenThemeDataForDpi function


## -description

A variant of <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> that opens a theme handle associated with a specific DPI.

## -parameters

### -param hwnd

The handle of the window for which theme data is required.

### -param pszClassList

A pointer to a string that contains a semicolon-separated list of classes.

### -param dpi

The specified DPI value with which to associate the theme handle. The function will return an error if this value is outside of those that correspond to the set of connected monitors.

## -returns

See <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>.

## -remarks

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> will create theme handles associated with the DPI of a window when used with Per Monitor v2 windows. OpenThemeDataForDpi allows you to open a theme handle for a specific DPI when you do not have a window at that DPI.

The behavior of the returned theme handle will be undermined if the requested DPI value does not correspond to a currently connected display. The theming system only loads theme assets for the set of DPI values corresponding to the <i>currently</i> connected displays.

The theme handle will become invalid anytime the system reloads the theme data. Applications are required to monitor <a href="/windows/desktop/winmsg/wm-themechanged">WM_THEMECHANGED</a> and close and reopen all theme handles in response. This behavior is the same regardless of whether the handles were opened via OpenThemeData or OpenThemeDataForDpi.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>