---
UID: NF:uxtheme.GetWindowTheme
title: GetWindowTheme function
author: windows-driver-content
description: Retrieves a theme handle to a window that has visual styles applied.
old-location: controls\GetWindowTheme.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getwindowtheme.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
-	xamlpalwp.dll
api_name:
-	GetWindowTheme
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
req.product: Windows UI
---

# GetWindowTheme function


## -description


Retrieves a theme handle to a window that has visual styles applied.


## -parameters




### -param hwnd

TBD




#### - hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the window.


## -returns



Type: <b>HTHEME</b>

The most recent theme handle from <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a>.




## -remarks



If a window has a visual style applied, the <b>GetWindowTheme</b> function returns the most recent theme handle from <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a>. If no visual style is applied, <b>GetWindowTheme</b> returns <b>NULL</b>.



