---
UID: NF:uxtheme.SetWindowThemeNonClientAttributes
title: SetWindowThemeNonClientAttributes function
author: windows-sdk-content
description: Sets non-client attributes to control how visual styles are applied to a specified window.
old-location: controls\SetWindowThemeNonClientAttributes.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowthemenonclientattributes.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: SetWindowThemeNonClientAttributes, SetWindowThemeNonClientAttributes function [Windows Controls], _shell_SetWindowThemeNonClientAttributes, _shell_SetWindowThemeNonClientAttributes_cpp, controls.SetWindowThemeNonClientAttributes, controls._shell_SetWindowThemeNonClientAttributes, uxtheme/SetWindowThemeNonClientAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
api_name:
 - SetWindowThemeNonClientAttributes
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# SetWindowThemeNonClientAttributes function


## -description


Sets non-client attributes to control how visual styles are applied to a specified window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window in which to apply changes.


### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A bitmask that describes which values are to be modified. Can be a combination of the <a href="https://msdn.microsoft.com/C71D1957-6572-4242-B715-C54BDFBBD6B7">WTNCA</a> constants.


### -param dwAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A combination of flags that modify window visual style attributes based on <i>dwMask</i>. Can be a combination of the <a href="https://msdn.microsoft.com/C71D1957-6572-4242-B715-C54BDFBBD6B7">WTNCA</a> constants.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



