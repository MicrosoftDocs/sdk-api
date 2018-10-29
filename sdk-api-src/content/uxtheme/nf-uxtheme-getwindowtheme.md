---
UID: NF:uxtheme.GetWindowTheme
title: GetWindowTheme function
author: windows-sdk-content
description: Retrieves a theme handle to a window that has visual styles applied.
old-location: controls\GetWindowTheme.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getwindowtheme.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetWindowTheme, GetWindowTheme function [Windows Controls], controls.GetWindowTheme, controls.inet_GetWindowTheme, inet_GetWindowTheme, inet_GetWindowTheme_cpp, uxtheme/GetWindowTheme
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
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - GetWindowTheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowTheme function


## -description


Retrieves a theme handle to a window that has visual styles applied.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the window.


## -returns



Type: <b>HTHEME</b>

The most recent theme handle from <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a>.




## -remarks



If a window has a visual style applied, the <b>GetWindowTheme</b> function returns the most recent theme handle from <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a>. If no visual style is applied, <b>GetWindowTheme</b> returns <b>NULL</b>.



