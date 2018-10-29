---
UID: NF:uxtheme.OpenThemeData
title: OpenThemeData function
author: windows-sdk-content
description: Opens the theme data for a window and its associated class.
old-location: controls\OpenThemeData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\openthemedata.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: OpenThemeData, OpenThemeData function [Windows Controls], controls.OpenThemeData, controls.inet_OpenThemeData, inet_OpenThemeData, inet_OpenThemeData_cpp, uxtheme/OpenThemeData
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
 - OpenThemeData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenThemeData function


## -description


Opens the theme data for a window and its associated class.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the window for which theme data is required.


### -param pszClassList [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains a semicolon-separated list of classes.


## -returns



Type: <b>HTHEME</b>

<b>OpenThemeData</b> tries to match each class, one at a time, to a class data section in the active theme. If a match is found, an associated HTHEME handle is returned. If no match is found <b>NULL</b> is returned.




## -remarks



The <i>pszClassList</i> parameter contains a list, not just a single name, to provide the class an opportunity to get the best match between the class and the current visual style. For example, a button might pass L"OkButton;Button" 
if its ID is ID_OK. If the current visual style has an entry for OkButton, that is used; otherwise no visual style is applied.

Class names for the Aero theme are defined in AeroStyle.xml.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773287(v=VS.85).aspx">CloseThemeData</a>
 

 

