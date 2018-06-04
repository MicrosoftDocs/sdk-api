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

# GetCharABCWidthsFloatW function


## -description


The <b>GetCharABCWidthsFloat</b> function retrieves the widths, in logical units, of consecutive characters in a specified range from the current font.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param iFirst

TBD


### -param iLast

TBD


### -param lpABC

TBD




#### - iFirstChar [in]

Specifies the code point of the first character in the group of consecutive characters where the ABC widths are seeked.


#### - iLastChar [in]

Specifies the code point of the last character in the group of consecutive characters where the ABC widths are seeked. This range is inclusive. An error is returned if the specified last character precedes the specified first character.


#### - lpABCF [out]

Pointer to an array of <a href="https://msdn.microsoft.com/540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0">ABCFLOAT</a> structures that receives the character widths, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a> function that returns widths only for TrueType fonts, the <b>GetCharABCWidthsFloat</b> function retrieves widths for any font. The widths returned by this function are in the IEEE floating-point format.

If the current world-to-device transformation is not identified, the returned widths may be noninteger values, even if the corresponding values in the device space are integers.

A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

The ABC spaces are measured along the character base line of the selected font.

The ABC widths of the default character are used for characters outside the range of the currently selected font.




## -see-also




<a href="https://msdn.microsoft.com/540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0">ABCFLOAT</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/be29c195-cf67-45d5-8a46-ac572afb756d">GetCharWidth</a>



<a href="https://msdn.microsoft.com/7a90b701-63f9-41e5-9069-10d344edfe02">GetCharWidthFloat</a>
 

 

