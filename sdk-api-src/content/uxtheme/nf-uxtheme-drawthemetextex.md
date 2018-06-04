---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DrawThemeTextEx function


## -description


Draws text using the color and font defined by the visual style. Extends <a href="https://msdn.microsoft.com/9f58909c-7ceb-4e30-8be7-f2de91cc38a8">DrawThemeText</a> by allowing additional text format options.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use for drawing.


### -param iPartId [in]

Type: <b>int</b>

The control part that has the desired text appearance. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>. If this value is 0, the text is drawn in the default font, or a font selected into the device context.


### -param iStateId [in]

Type: <b>int</b>

The control state that has the desired text appearance. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pszText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.


### -param cchText

TBD


### -param dwTextFlags

TBD


### -param pRect [in, out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle, in logical coordinates, in which the text is to be drawn.


### -param pOptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/4e20afab-a607-4107-a71c-a29589a8fc1f">DTTOPTS</a>*</b>

A <a href="https://msdn.microsoft.com/4e20afab-a607-4107-a71c-a29589a8fc1f">DTTOPTS</a> structure that defines additional formatting options that will be applied to the text being drawn.


#### - dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="https://msdn.microsoft.com/765b90df-4753-43e6-bcf7-6512f6f378bd">Format Values</a> for possible parameter values.


#### - iCharCount [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function always uses the themed font for the specified part and state if one is defined. Otherwise it uses the font currently selected into the device context. To find out if a themed font is defined, you can call <a href="https://msdn.microsoft.com/8ecfd467-1dcf-46bc-9b49-61c11714b45d">GetThemeFont</a> or <a href="https://msdn.microsoft.com/6b7f298c-1b3d-463d-a5ec-fbe72672ef49">GetThemePropertyOrigin</a> with TMT_FONT as the property identifier.



