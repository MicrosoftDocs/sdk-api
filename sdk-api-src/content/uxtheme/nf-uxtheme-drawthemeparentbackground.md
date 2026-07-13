---
UID: NF:uxtheme.DrawThemeParentBackground
title: DrawThemeParentBackground function (uxtheme.h)
description: Draws the part of a parent control that is covered by a partially-transparent or alpha-blended child control.
helpviewer_keywords: ["DrawThemeParentBackground","DrawThemeParentBackground function [Windows Controls]","controls.DrawThemeParentBackground","controls.inet_DrawThemeParentBackground","inet_DrawThemeParentBackground","inet_DrawThemeParentBackground_cpp","uxtheme/DrawThemeParentBackground"]
old-location: controls\DrawThemeParentBackground.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeparentbackground.htm
ms.date: 12/05/2018
ms.keywords: DrawThemeParentBackground, DrawThemeParentBackground function [Windows Controls], controls.DrawThemeParentBackground, controls.inet_DrawThemeParentBackground, inet_DrawThemeParentBackground, inet_DrawThemeParentBackground_cpp, uxtheme/DrawThemeParentBackground
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawThemeParentBackground
 - uxtheme/DrawThemeParentBackground
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeParentBackground
---

# DrawThemeParentBackground function


## -description

Draws the part of a parent control that is covered by a partially-transparent or alpha-blended child control.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The child control.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

The child control's DC.

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The area to be drawn. The rectangle is in the child window's coordinates. If this parameter is NULL, the area to be drawn includes the entire area occupied by the child control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.