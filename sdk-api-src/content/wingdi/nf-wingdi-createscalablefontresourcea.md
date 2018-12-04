---
UID: NF:wingdi.CreateScalableFontResourceA
title: CreateScalableFontResourceA function
author: windows-sdk-content
description: The CreateScalableFontResource function creates a font resource file for a scalable font.
old-location: gdi\createscalablefontresource.htm
tech.root: gdi
ms.assetid: 9a43a254-4cf4-46de-80b2-a83838871fd7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 0, 1, CreateScalableFontResource, CreateScalableFontResource function [Windows GDI], CreateScalableFontResourceA, CreateScalableFontResourceW, _win32_CreateScalableFontResource, gdi.createscalablefontresource, wingdi/CreateScalableFontResource, wingdi/CreateScalableFontResourceA, wingdi/CreateScalableFontResourceW
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
req.unicode-ansi: CreateScalableFontResourceW (Unicode) and CreateScalableFontResourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateScalableFontResource
 - CreateScalableFontResourceA
 - CreateScalableFontResourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateScalableFontResourceA function


## -description


<p class="CCE_Message">[The <b>CreateScalableFontResource</b> function is available for use in the operating systems specified in the Requirements section. It may be 

altered or unavailable in subsequent versions.]

The <b>CreateScalableFontResource</b> function creates a font resource file for a scalable font.


## -parameters




### -param fdwHidden [in]

Specifies whether the font is a read-only font. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The font has read/write permission.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The font has read-only permission and should be hidden from other applications in the system. When this flag is set, the font is not enumerated by the <a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a> or <a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a> function.

</td>
</tr>
</table>
 


### -param lpszFont [in]

A pointer to a null-terminated string specifying the name of the font resource file to create. If this parameter specifies an existing font resource file, the function fails.


### -param lpszFile [in]

A pointer to a null-terminated string specifying the name of the scalable font file that this function uses to create the font resource file.


### -param lpszPath [in]

A pointer to a null-terminated string specifying the path to the scalable font file.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

If <i>lpszFontRes</i> specifies an existing font file, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_FILE_EXISTS




## -remarks



The <b>CreateScalableFontResource</b> function is used by applications that install TrueType fonts. An application uses the <b>CreateScalableFontResource</b> function to create a font resource file (typically with a .fot file name extension) and then uses the <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> function to install the font. The TrueType font file (typically with a .ttf file name extension) must be in the System subdirectory of the Windows directory to be used by the <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> function.

The <b>CreateScalableFontResource</b> function currently supports only TrueType-technology scalable fonts.

When the <i>lpszFontFile</i> parameter specifies only a file name and extension, the <i>lpszCurrentPath</i> parameter must specify a path. When the <i>lpszFontFile</i> parameter specifies a full path, the <i>lpszCurrentPath</i> parameter must be <b>NULL</b> or a pointer to <b>NULL</b>.

When only a file name and extension are specified in the <i>lpszFontFile</i> parameter and a path is specified in the <i>lpszCurrentPath</i> parameter, the string in <i>lpszFontFile</i> is copied into the .fot file as the .ttf file that belongs to this resource. When the <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> function is called, the operating system assumes that the .ttf file has been copied into the System directory (or into the main Windows directory in the case of a network installation). The .ttf file need not be in this directory when the <b>CreateScalableFontResource</b> function is called, because the <i>lpszCurrentPath</i> parameter contains the directory information. A resource created in this manner does not contain absolute path information and can be used in any installation.

When a path is specified in the <i>lpszFontFile</i> parameter and <b>NULL</b> is specified in the <i>lpszCurrentPath</i> parameter, the string in <i>lpszFontFile</i> is copied into the .fot file. In this case, when the <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> function is called, the .ttf file must be at the location specified in the <i>lpszFontFile</i> parameter when the <b>CreateScalableFontResource</b> function was called; the <i>lpszCurrentPath</i> parameter is not needed. A resource created in this manner contains absolute references to paths and drives and does not work if the .ttf file is moved to a different location.




## -see-also




<a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource
      </a>



<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies
      </a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts
      </a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

