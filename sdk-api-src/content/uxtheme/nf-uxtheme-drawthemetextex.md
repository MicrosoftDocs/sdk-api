---
UID: NF:uxtheme.DrawThemeTextEx
title: DrawThemeTextEx function
author: windows-sdk-content
description: Draws text using the color and font defined by the visual style. Extends DrawThemeText by allowing additional text format options.
old-location: controls\DrawThemeTextEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemetextex.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DrawThemeTextEx, DrawThemeTextEx function [Windows Controls], controls.DrawThemeTextEx, controls.inet_DrawThemeTextEx, inet_DrawThemeTextEx, inet_DrawThemeTextEx_cpp, uxtheme/DrawThemeTextEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeTextEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawThemeTextEx function


## -description


Draws text using the color and font defined by the visual style. Extends <a href="https://msdn.microsoft.com/en-us/library/Bb773312(v=VS.85).aspx">DrawThemeText</a> by allowing additional text format options.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use for drawing.


### -param iPartId [in]

Type: <b>int</b>

The control part that has the desired text appearance. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>. If this value is 0, the text is drawn in the default font, or a font selected into the device context.


### -param iStateId [in]

Type: <b>int</b>

The control state that has the desired text appearance. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pszText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.


### -param cchText [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.


### -param dwTextFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="https://msdn.microsoft.com/en-us/library/Bb773199(v=VS.85).aspx">Format Values</a> for possible parameter values.


### -param pRect [in, out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle, in logical coordinates, in which the text is to be drawn.


### -param pOptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb773236(v=VS.85).aspx">DTTOPTS</a>*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb773236(v=VS.85).aspx">DTTOPTS</a> structure that defines additional formatting options that will be applied to the text being drawn.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function always uses the themed font for the specified part and state if one is defined. Otherwise it uses the font currently selected into the device context. To find out if a themed font is defined, you can call <a href="https://msdn.microsoft.com/en-us/library/Bb759745(v=VS.85).aspx">GetThemeFont</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb759764(v=VS.85).aspx">GetThemePropertyOrigin</a> with TMT_FONT as the property identifier.



