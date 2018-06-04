---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# OpenThemeDataForDpi function


## -description


A variant of <a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a> that opens a theme handle associated with a specific DPI.


## -parameters




### -param hwnd

The handle of the window for which theme data is required.


### -param pszClassList

TBD


### -param dpi

The specified DPI value with which to associate the theme handle. The function will return an error if this value is outside of those that correspond to the set of connected monitors.


#### - pszClassIdList

A pointer to a string that contains a semicolon-separated list of classes.


## -returns



See <a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a>.




## -remarks



<a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a> will create theme handles associated with the DPI of a window when used with Per Monitor v2 windows. OpenThemeDataForDpi allows you to open a theme handle for a specific DPI when you do not have a window at that DPI.

The behavior of the returned theme handle will be undermined if the requested DPI value does not correspond to a currently connected display. The theming system only loads theme assets for the set of DPI values corresponding to the <i>currently</i> connected displays.

The theme handle will become invalid anytime the system reloads the theme data. Applications are required to monitor <a href="https://msdn.microsoft.com/library/windows/desktop/ms632650(v=vs.85)">WM_THEMECHANGED</a> and close and reopen all theme handles in response. This behavior is the same regardless of whether the handles were opened via OpenThemeData or OpenThemeDataForDpi.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/desktop/bb759821(v=vs.85)">OpenThemeData</a>
 

 

