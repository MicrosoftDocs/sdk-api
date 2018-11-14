---
UID: NF:uxtheme.GetThemeTextExtent
title: GetThemeTextExtent function
author: windows-sdk-content
description: Calculates the size and location of the specified text when rendered in the visual style font.
old-location: controls\GetThemeTextExtent.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetextextent.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetThemeTextExtent, GetThemeTextExtent function [Windows Controls], controls.GetThemeTextExtent, controls.inet_GetThemeTextExtent, inet_GetThemeTextExtent, inet_GetThemeTextExtent_cpp, uxtheme/GetThemeTextExtent
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
api_name:
 - GetThemeTextExtent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetThemeTextExtent
: 
---

# GetThemeTextExtent function


## -description


Calculates the size and location of the specified text when rendered in the visual style font.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to select the font into.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part in which the text will be drawn. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pszText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.


### -param cchCharCount [in]

Type: <b>int</b>

Value of type<b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.


### -param dwTextFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="https://msdn.microsoft.com/en-us/library/Bb773199(v=VS.85).aspx">Format Values</a> for possible parameter values. 
	


### -param pBoundingRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle used to control layout of the text. This parameter may be set to <b>NULL</b>.


### -param pExtentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains, in logical coordinates, the rectangle required to fit the rendered text.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>
 

 

