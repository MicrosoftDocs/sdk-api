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

# EnumFontFamiliesW function


## -description


The <b>EnumFontFamilies</b> function enumerates the fonts in a specified font family that are available on a specified device.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> function.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to the device context from which to enumerate the fonts.


### -param lpLogfont

TBD


### -param lpProc

TBD


### -param lParam [in]

A pointer to application-supplied data. The data is passed to the callback function along with the font information.


#### - lpEnumFontFamProc [in]

A pointer to the application defined callback function. For information, see <a href="https://msdn.microsoft.com/9957885a-abf7-4d7c-ae8d-40f5d1150591">EnumFontFamProc</a>.


#### - lpszFamily [in]

A pointer to a null-terminated string that specifies the family name of the desired fonts. If <i>lpszFamily</i> is <b>NULL</b>, <b>EnumFontFamilies</b> selects and enumerates one font of each available type family.


## -returns



The return value is the last value returned by the callback function. Its meaning is implementation specific.




## -remarks



For each font having the typeface name specified by the <i>lpszFamily</i> parameter, the <b>EnumFontFamilies</b> function retrieves information about that font and passes it to the function pointed to by the <i>lpEnumFontFamProc</i> parameter. The application defined callback function can process the font information as desired. Enumeration continues until there are no more fonts or the callback function returns zero.

When the graphics mode on the device context is set to GM_ADVANCED using the SetGraphicsMode function and the DEVICE_FONTTYPE flag is passed to the FontType parameter, this function returns a list of type 1 and OpenType fonts on the system. When the graphics mode is not set to GM_ADVANCED, this function returns a list of type 1, OpenType, and TrueType fonts on the system.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>, <b>EnumFontFamilies</b>, and <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.


#### Examples

For examples, see <a href="https://msdn.microsoft.com/18db1b03-6e3c-4be3-b637-a21bf41cc080">Enumerating the Installed Fonts</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9957885a-abf7-4d7c-ae8d-40f5d1150591">EnumFontFamProc</a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

