---
UID: NF:uxtheme.CloseThemeData
title: CloseThemeData function (uxtheme.h)
description: Closes the theme data handle.
helpviewer_keywords: ["CloseThemeData","CloseThemeData function [Windows Controls]","controls.CloseThemeData","controls.inet_CloseThemeData","inet_CloseThemeData","inet_CloseThemeData_cpp","uxtheme/CloseThemeData"]
old-location: controls\CloseThemeData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\closethemedata.htm
ms.date: 12/05/2018
ms.keywords: CloseThemeData, CloseThemeData function [Windows Controls], controls.CloseThemeData, controls.inet_CloseThemeData, inet_CloseThemeData, inet_CloseThemeData_cpp, uxtheme/CloseThemeData
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
 - CloseThemeData
 - uxtheme/CloseThemeData
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - CloseThemeData
---

# CloseThemeData function


## -description

Closes the theme data handle.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an <b>HTHEME</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>CloseThemeData</b> function should be called when a window that has a visual style applied is destroyed. This function should also be called whenever a window receives a <a href="/windows/desktop/winmsg/wm-themechanged">WM_THEMECHANGED</a> message. This call should be followed by an attempt to create a new theme data handle if a call to the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-isthemeactive">IsThemeActive</a> function returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a>