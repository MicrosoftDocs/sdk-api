---
UID: NF:wingdi.EnumFontsA
title: EnumFontsA function
author: windows-driver-content
description: The EnumFonts function enumerates the fonts available on a specified device.
old-location: gdi\enumfonts.htm
old-project: gdi
ms.assetid: b5dfc38d-c400-4900-a15b-f251815ee346
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: EnumFonts, EnumFonts function [Windows GDI], EnumFontsA, EnumFontsW, _win32_EnumFonts, gdi.enumfonts, wingdi/EnumFonts, wingdi/EnumFontsA, wingdi/EnumFontsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFontsW (Unicode) and EnumFontsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Font-L1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	EnumFonts
-	EnumFontsA
-	EnumFontsW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumFontsA function


## -description


The <b>EnumFonts</b> function enumerates the fonts available on a specified device. For each font with the specified typeface name, the <b>EnumFonts</b> function retrieves information about that font and passes it to the application defined callback function. This callback function can process the font information as desired. Enumeration continues until there are no more fonts or the callback function returns zero.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> function.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to the device context from which to enumerate the fonts.


### -param lpLogfont

TBD


### -param lpProc

TBD


### -param lParam [in]

A pointer to any application-defined data. The data is passed to the callback function along with the font information.


#### - lpFaceName [in]

A pointer to a null-terminated string that specifies the typeface name of the desired fonts. If <i>lpFaceName</i> is <b>NULL</b>, <b>EnumFonts</b> randomly selects and enumerates one font of each available typeface.


#### - lpFontFunc [in]

A pointer to the application definedcallback function. For more information, see <a href="https://msdn.microsoft.com/23401bf9-50f9-4bc1-9fd6-dcb4c22d38f7">EnumFontsProc</a>.


## -returns



The return value is the last value returned by the callback function. Its meaning is defined by the application.




## -remarks



Use <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> instead of <b>EnumFonts</b>. The <b>EnumFontFamiliesEx</b> function differs from the <b>EnumFonts</b> function in that it retrieves the style names associated with a TrueType font. With <b>EnumFontFamiliesEx</b>, you can retrieve information about font styles that cannot be enumerated using the <b>EnumFonts</b> function.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <b>EnumFonts</b>, <a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>, and <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.




## -see-also




<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a>



<a href="https://msdn.microsoft.com/23401bf9-50f9-4bc1-9fd6-dcb4c22d38f7">EnumFontsProc</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>
 

 

