---
UID: NF:uxtheme.SetWindowTheme
title: SetWindowTheme function
author: windows-sdk-content
description: Causes a window to use a different set of visual style information than its class normally uses.
old-location: controls\SetWindowTheme.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowtheme.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetWindowTheme, SetWindowTheme function [Windows Controls], controls.SetWindowTheme, controls.inet_SetWindowTheme, inet_SetWindowTheme, inet_SetWindowTheme_cpp, uxtheme/SetWindowTheme
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
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
 - SetWindowTheme
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# SetWindowTheme function


## -description


Causes a window to use a different set of visual style information than its class normally uses.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the window whose visual style information is to be changed.


### -param pszSubAppName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the application name to use in place of the calling application's name. If this parameter is <b>NULL</b>, the calling application's name is used.


### -param pszSubIdList [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains a semicolon-separated list of CLSID names to use in place of the actual list passed by the window's class. If this parameter is <b>NULL</b>, the ID list from the calling class is used.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The theme manager retains the <i>pszSubAppName</i> and the <i>pszSubIdList</i> associations through the lifetime of the window, even if visual styles subsequently change. The window is sent a <a href="https://msdn.microsoft.com/en-us/library/ms632650(v=VS.85).aspx">WM_THEMECHANGED</a> message at the end of a <b>SetWindowTheme</b> call, so that the new visual style can be found and applied.


When <i>pszSubAppName</i> and <i>pszSubIdList</i> are <b>NULL</b>, the theme manager removes the previously applied associations. You can prevent visual styles from being applied to a specified window by specifying an empty string, (L" "), which does not match any section entries. 


#### Examples

The following example code gives a list-view control the appearance of a Windows Explorer list: 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SetWindowTheme(hwndList, L"Explorer", NULL);
</pre>
</td>
</tr>
</table></span></div>


