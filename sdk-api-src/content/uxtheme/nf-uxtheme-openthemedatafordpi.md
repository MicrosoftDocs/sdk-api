---
UID: NF:uxtheme.OpenThemeDataForDpi
title: OpenThemeDataForDpi function
author: windows-sdk-content
description: A variant of OpenThemeData that opens a theme handle associated with a specific DPI.
old-location: hidpi\openthemedatafordpi.htm
old-project: hidpi
ms.assetid: 40044856-82F2-47E2-AD4B-5E4F3868E7B8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OpenThemeDataForDpi, OpenThemeDataForDpi function [High DPI], hidpi.openthemedatafordpi, uxtheme/OpenThemeDataForDpi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - OpenThemeDataForDpi
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows UI
---

# OpenThemeDataForDpi function


## -description


A variant of <a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a> that opens a theme handle associated with a specific DPI.


## -parameters




### -param hwnd

The handle of the window for which theme data is required.


### -param pszClassList

A pointer to a string that contains a semicolon-separated list of classes.


### -param dpi

The specified DPI value with which to associate the theme handle. The function will return an error if this value is outside of those that correspond to the set of connected monitors.


## -returns



See <a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a>.




## -remarks



<a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a> will create theme handles associated with the DPI of a window when used with Per Monitor v2 windows. OpenThemeDataForDpi allows you to open a theme handle for a specific DPI when you do not have a window at that DPI.

The behavior of the returned theme handle will be undermined if the requested DPI value does not correspond to a currently connected display. The theming system only loads theme assets for the set of DPI values corresponding to the <i>currently</i> connected displays.

The theme handle will become invalid anytime the system reloads the theme data. Applications are required to monitor <a href="https://msdn.microsoft.com/library/windows/desktop/ms632650(v=vs.85)">WM_THEMECHANGED</a> and close and reopen all theme handles in response. This behavior is the same regardless of whether the handles were opened via OpenThemeData or OpenThemeDataForDpi.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a>
 

 

