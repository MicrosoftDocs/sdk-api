---
UID: NF:uxtheme.OpenThemeDataEx
title: OpenThemeDataEx function
author: windows-sdk-content
description: Opens the theme data associated with a window for specified theme classes.
old-location: controls\OpenThemeDataEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\openthemedataex.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: OTD_FORCE_RECT_SIZING, OTD_NONCLIENT, OpenThemeDataEx, OpenThemeDataEx function [Windows Controls], controls.OpenThemeDataEx, controls.inet_OpenThemeDataEx, inet_OpenThemeDataEx, inet_OpenThemeDataEx_cpp, uxtheme/OpenThemeDataEx
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - OpenThemeDataEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenThemeDataEx
: 
---

# OpenThemeDataEx function


## -description


Opens the theme data associated with a window for specified theme classes.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a window or control that the theme is to be retrieved from.


### -param pszClassList [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A semicolon-separated list of class names to match.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Optional flags that control how to return the theme data. May be set to a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OTD_FORCE_RECT_SIZING"></a><a id="otd_force_rect_sizing"></a><dl>
<dt><b>OTD_FORCE_RECT_SIZING</b></dt>
</dl>
</td>
<td width="60%">
Forces drawn images from this theme to stretch to fit the rectangles specified by drawing functions.

</td>
</tr>
<tr>
<td width="40%"><a id="OTD_NONCLIENT"></a><a id="otd_nonclient"></a><dl>
<dt><b>OTD_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Allows theme elements to be drawn in the non-client area of the window.

</td>
</tr>
</table>
 


## -returns



Type: <b>HTHEME</b>

If a match is found, a valid handle to a theme is returned. Otherwise, a <b>NULL</b> value will be returned.




## -remarks



The string specified by <i>pszClassIdList</i> will be tokenized using semicolons as a delimiter. The names are matched against class names one token at a time. If no match is found for a particular token, the next token will be matched. If a match is found, the return value of the function will be the theme handle associated with the matched class.

Class names for the Aero theme are defined in AeroStyle.xml.




## -see-also




<a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a>
 

 

