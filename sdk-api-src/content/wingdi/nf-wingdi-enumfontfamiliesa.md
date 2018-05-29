---
UID: NF:wingdi.EnumFontFamiliesA
title: EnumFontFamiliesA function
author: windows-sdk-content
description: The EnumFontFamilies function enumerates the fonts in a specified font family that are available on a specified device.
old-location: gdi\enumfontfamilies.htm
old-project: gdi
ms.assetid: 4960afbb-eeba-4030-ac89-d1ff077bb2f3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: EnumFontFamilies, EnumFontFamilies function [Windows GDI], EnumFontFamiliesA, EnumFontFamiliesW, _win32_EnumFontFamilies, gdi.enumfontfamilies, wingdi/EnumFontFamilies, wingdi/EnumFontFamiliesA, wingdi/EnumFontFamiliesW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFontFamiliesW (Unicode) and EnumFontFamiliesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-0.dll
-	Ext-MS-Win-GDI-Font-l1-1-1.dll
-	ext-ms-win-gdi-font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	EnumFontFamilies
-	EnumFontFamiliesA
-	EnumFontFamiliesW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumFontFamiliesA function


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
 

 

