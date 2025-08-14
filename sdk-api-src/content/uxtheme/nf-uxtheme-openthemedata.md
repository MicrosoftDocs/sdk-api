---
UID: NF:uxtheme.OpenThemeData
title: OpenThemeData function (uxtheme.h)
description: Opens the theme data for a window and its associated class.
helpviewer_keywords: ["OpenThemeData","OpenThemeData function [Windows Controls]","controls.OpenThemeData","controls.inet_OpenThemeData","inet_OpenThemeData","inet_OpenThemeData_cpp","uxtheme/OpenThemeData"]
old-location: controls\OpenThemeData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\openthemedata.htm
ms.date: 12/05/2018
ms.keywords: OpenThemeData, OpenThemeData function [Windows Controls], controls.OpenThemeData, controls.inet_OpenThemeData, inet_OpenThemeData, inet_OpenThemeData_cpp, uxtheme/OpenThemeData
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
 - OpenThemeData
 - uxtheme/OpenThemeData
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
 - OpenThemeData
---

# OpenThemeData function


## -description

Opens the theme data for a window and its associated class.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle of the window for which theme data is required.

### -param pszClassList [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains a semicolon-separated list of classes.

## -returns

Type: <b>HTHEME</b>

<b>OpenThemeData</b> tries to match each class, one at a time, to a class data section in the active theme. If a match is found, an associated HTHEME handle is returned. If no match is found <b>NULL</b> is returned.

## -remarks

The <i>pszClassList</i> parameter contains a list, not just a single name, to provide the class an opportunity to get the best match between the class and the current visual style. For example, a button might pass L"OkButton;Button" 
if its ID is ID_OK. If the current visual style has an entry for OkButton, that is used; otherwise no visual style is applied.

Class names for the Aero theme are defined in AeroStyle.xml.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-closethemedata">CloseThemeData</a>