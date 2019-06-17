---
UID: NF:uxtheme.GetThemeSysColor
title: GetThemeSysColor function (uxtheme.h)
author: windows-sdk-content
description: Retrieves the value of a system color.
old-location: controls\GetThemeSysColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesyscolor.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThemeSysColor, GetThemeSysColor function [Windows Controls], controls.GetThemeSysColor, controls.inet_GetThemeSysColor, inet_GetThemeSysColor, inet_GetThemeSysColor_cpp, uxtheme/GetThemeSysColor
ms.topic: function
f1_keywords: ["uxtheme/GetThemeSysColor"]
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeSysColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThemeSysColor function


## -description


Retrieves the value of a system color.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.


### -param iColorId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the color number. May be one of the values listed in <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> for the <i>nIndex</i> parameter.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The value of the specified system color.




## -remarks



If the theme data handle is not a <b>NULL</b> handle, this function returns the color from the SysMetrics section of the current visual style. If the theme data handle is <b>NULL</b>, this function returns the color matching the global system color.



