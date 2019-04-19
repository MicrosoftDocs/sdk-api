---
UID: NF:uxtheme.DrawThemeParentBackground
title: DrawThemeParentBackground function (uxtheme.h)
author: windows-sdk-content
description: Draws the part of a parent control that is covered by a partially-transparent or alpha-blended child control.
old-location: controls\DrawThemeParentBackground.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeparentbackground.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawThemeParentBackground, DrawThemeParentBackground function [Windows Controls], controls.DrawThemeParentBackground, controls.inet_DrawThemeParentBackground, inet_DrawThemeParentBackground, inet_DrawThemeParentBackground_cpp, uxtheme/DrawThemeParentBackground
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
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeParentBackground
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawThemeParentBackground function


## -description


Draws the part of a parent control that is covered by a partially-transparent or alpha-blended child control.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The child control.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The child control's DC.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The area to be drawn. The rectangle is in the child window's coordinates. If this parameter is NULL, the area to be drawn includes the entire area occupied by the child control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



