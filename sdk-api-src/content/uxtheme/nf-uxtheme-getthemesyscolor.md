---
UID: NF:uxtheme.GetThemeSysColor
title: GetThemeSysColor function
author: windows-sdk-content
description: Retrieves the value of a system color.
old-location: controls\GetThemeSysColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesyscolor.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetThemeSysColor, GetThemeSysColor function [Windows Controls], controls.GetThemeSysColor, controls.inet_GetThemeSysColor, inet_GetThemeSysColor, inet_GetThemeSysColor_cpp, uxtheme/GetThemeSysColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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

Value of type <b>int</b> that specifies the color number. May be one of the values listed in <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> for the <i>nIndex</i> parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The value of the specified system color.




## -remarks



If the theme data handle is not a <b>NULL</b> handle, this function returns the color from the SysMetrics section of the current visual style. If the theme data handle is <b>NULL</b>, this function returns the color matching the global system color.



