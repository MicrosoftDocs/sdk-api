---
UID: NF:uxtheme.GetCurrentThemeName
title: GetCurrentThemeName function
author: windows-driver-content
description: Retrieves the name of the current visual style, and optionally retrieves the color scheme name and size name.
old-location: controls\GetCurrentThemeName.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getcurrentthemename.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetCurrentThemeName, GetCurrentThemeName function [Windows Controls], controls.GetCurrentThemeName, controls.inet_GetCurrentThemeName, inet_GetCurrentThemeName, inet_GetCurrentThemeName_cpp, uxtheme/GetCurrentThemeName
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
api_name:
-	GetCurrentThemeName
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
req.product: Windows UI
---

# GetCurrentThemeName function


## -description


Retrieves the name of the current visual style, and optionally retrieves the color scheme name and size name.


## -parameters




### -param pszThemeFileName [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the theme path and file name.


### -param cchMaxNameChars

TBD


### -param pszColorBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the color scheme name. This parameter may be set to <b>NULL</b>.


### -param cchMaxColorChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the color scheme name.


### -param pszSizeBuff [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a string that receives the size name. This parameter may be set to <b>NULL</b>.


### -param cchMaxSizeChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the size name.


#### - dwMaxNameChars [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the maximum number of characters allowed in the theme file name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.



