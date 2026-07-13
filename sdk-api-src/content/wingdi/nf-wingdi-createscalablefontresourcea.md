---
UID: NF:wingdi.CreateScalableFontResourceA
title: CreateScalableFontResourceA function (wingdi.h)
description: The CreateScalableFontResource function creates a font resource file for a scalable font. (ANSI)
helpviewer_keywords: ["0", "1", "CreateScalableFontResourceA", "wingdi/CreateScalableFontResourceA"]
old-location: gdi\createscalablefontresource.htm
tech.root: gdi
ms.assetid: 9a43a254-4cf4-46de-80b2-a83838871fd7
ms.date: 12/05/2018
ms.keywords: 0, 1, CreateScalableFontResource, CreateScalableFontResource function [Windows GDI], CreateScalableFontResourceA, CreateScalableFontResourceW, _win32_CreateScalableFontResource, gdi.createscalablefontresource, wingdi/CreateScalableFontResource, wingdi/CreateScalableFontResourceA, wingdi/CreateScalableFontResourceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateScalableFontResourceA
 - wingdi/CreateScalableFontResourceA
dev_langs:
 - c++
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
The font has read-only permission and should be hidden from other applications in the system. When this flag is set, the font is not enumerated by the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a> function.

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

If <i>lpszFontRes</i> specifies an existing font file, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_FILE_EXISTS

## -remarks

The <b>CreateScalableFontResource</b> function is used by applications that install TrueType fonts. An application uses the <b>CreateScalableFontResource</b> function to create a font resource file (typically with a .fot file name extension) and then uses the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> function to install the font. The TrueType font file (typically with a .ttf file name extension) must be in the System subdirectory of the Windows directory to be used by the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> function.

The <b>CreateScalableFontResource</b> function currently supports only TrueType-technology scalable fonts.

When the <i>lpszFontFile</i> parameter specifies only a file name and extension, the <i>lpszCurrentPath</i> parameter must specify a path. When the <i>lpszFontFile</i> parameter specifies a full path, the <i>lpszCurrentPath</i> parameter must be <b>NULL</b> or a pointer to <b>NULL</b>.

When only a file name and extension are specified in the <i>lpszFontFile</i> parameter and a path is specified in the <i>lpszCurrentPath</i> parameter, the string in <i>lpszFontFile</i> is copied into the .fot file as the .ttf file that belongs to this resource. When the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> function is called, the operating system assumes that the .ttf file has been copied into the System directory (or into the main Windows directory in the case of a network installation). The .ttf file need not be in this directory when the <b>CreateScalableFontResource</b> function is called, because the <i>lpszCurrentPath</i> parameter contains the directory information. A resource created in this manner does not contain absolute path information and can be used in any installation.

When a path is specified in the <i>lpszFontFile</i> parameter and <b>NULL</b> is specified in the <i>lpszCurrentPath</i> parameter, the string in <i>lpszFontFile</i> is copied into the .fot file. In this case, when the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> function is called, the .ttf file must be at the location specified in the <i>lpszFontFile</i> parameter when the <b>CreateScalableFontResource</b> function was called; the <i>lpszCurrentPath</i> parameter is not needed. A resource created in this manner contains absolute references to paths and drives and does not work if the .ttf file is moved to a different location.





> [!NOTE]
> The wingdi.h header defines CreateScalableFontResource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
