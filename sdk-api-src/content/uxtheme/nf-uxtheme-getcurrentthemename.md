---
UID: NF:uxtheme.GetCurrentThemeName
title: GetCurrentThemeName function (uxtheme.h)
description: Retrieves the name of the current visual style, and optionally retrieves the color scheme name and size name.
helpviewer_keywords: ["GetCurrentThemeName","GetCurrentThemeName function [Windows Controls]","controls.GetCurrentThemeName","controls.inet_GetCurrentThemeName","inet_GetCurrentThemeName","inet_GetCurrentThemeName_cpp","uxtheme/GetCurrentThemeName"]
old-location: controls\GetCurrentThemeName.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getcurrentthemename.htm
ms.date: 12/05/2018
ms.keywords: GetCurrentThemeName, GetCurrentThemeName function [Windows Controls], controls.GetCurrentThemeName, controls.inet_GetCurrentThemeName, inet_GetCurrentThemeName, inet_GetCurrentThemeName_cpp, uxtheme/GetCurrentThemeName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentThemeName
 - uxtheme/GetCurrentThemeName
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
api_name:
 - GetCurrentThemeName
---

# GetCurrentThemeName function


## -description

Retrieves the name of the current visual style, and optionally retrieves the color scheme name and size name.

## -parameters

### -param pszThemeFileName [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a string that receives the theme path and file name.

### -param cchMaxNameChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the theme file name.

### -param pszColorBuff [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a string that receives the color scheme name. This parameter may be set to <b>NULL</b>.

### -param cchMaxColorChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the color scheme name.

### -param pszSizeBuff [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a string that receives the size name. This parameter may be set to <b>NULL</b>.

### -param cchMaxSizeChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the size name.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.