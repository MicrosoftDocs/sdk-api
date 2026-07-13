---
UID: NF:wingdi.AddFontResourceW
title: AddFontResourceW function (wingdi.h)
description: The AddFontResource function adds the font resource from the specified file to the system font table. The font can subsequently be used for text output by any application. (Unicode)
helpviewer_keywords: [".fnt", ".fon", ".fot", ".mmm", ".otf", ".pfb", ".pfm", ".ttc", ".ttf", "AddFontResource", "AddFontResource function [Windows GDI]", "AddFontResourceW", "_win32_AddFontResource", "gdi.addfontresource", "wingdi/AddFontResource", "wingdi/AddFontResourceW"]
old-location: gdi\addfontresource.htm
tech.root: gdi
ms.assetid: e553a25a-f281-4ddc-8e95-1f61ed8238f9
ms.date: 12/05/2018
ms.keywords: .fnt, .fon, .fot, .mmm, .otf, .pfb, .pfm, .ttc, .ttf, AddFontResource, AddFontResource function [Windows GDI], AddFontResourceA, AddFontResourceW, _win32_AddFontResource, gdi.addfontresource, wingdi/AddFontResource, wingdi/AddFontResourceA, wingdi/AddFontResourceW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddFontResourceW (Unicode) and AddFontResourceA (ANSI)
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
 - AddFontResourceW
 - wingdi/AddFontResourceW
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
 - AddFontResource
 - AddFontResourceA
 - AddFontResourceW
---

# AddFontResourceW function


## -description

The <b>AddFontResource</b> function adds the font resource from the specified file to the system font table. The font can subsequently be used for text output by any application.

To mark a font as private or not enumerable, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a> function.

## -parameters

### -param unnamedParam1 [in]

A pointer to a null-terminated character string that contains a valid font file name. This parameter can specify any of the following files.

<table>
<tr>
<th>File Extension</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=".fon"></a><a id=".FON"></a><dl>
<dt><b>.fon</b></dt>
</dl>
</td>
<td width="60%">
Font resource file.

</td>
</tr>
<tr>
<td width="40%"><a id=".fnt"></a><a id=".FNT"></a><dl>
<dt><b>.fnt</b></dt>
</dl>
</td>
<td width="60%">
Raw bitmap font file.

</td>
</tr>
<tr>
<td width="40%"><a id=".ttf"></a><a id=".TTF"></a><dl>
<dt><b>.ttf</b></dt>
</dl>
</td>
<td width="60%">
Raw TrueType file.

</td>
</tr>
<tr>
<td width="40%"><a id=".ttc"></a><a id=".TTC"></a><dl>
<dt><b>.ttc</b></dt>
</dl>
</td>
<td width="60%">
East Asian Windows: TrueType font collection.

</td>
</tr>
<tr>
<td width="40%"><a id=".fot"></a><a id=".FOT"></a><dl>
<dt><b>.fot</b></dt>
</dl>
</td>
<td width="60%">
TrueType resource file.

</td>
</tr>
<tr>
<td width="40%"><a id=".otf"></a><a id=".OTF"></a><dl>
<dt><b>.otf</b></dt>
</dl>
</td>
<td width="60%">
PostScript OpenType font.

</td>
</tr>
<tr>
<td width="40%"><a id=".mmm"></a><a id=".MMM"></a><dl>
<dt><b>.mmm</b></dt>
</dl>
</td>
<td width="60%">
Multiple master Type1 font resource file. It must be used with .pfm and .pfb files.

</td>
</tr>
<tr>
<td width="40%"><a id=".pfb"></a><a id=".PFB"></a><dl>
<dt><b>.pfb</b></dt>
</dl>
</td>
<td width="60%">
Type 1 font bits file. It is used with a .pfm file.

</td>
</tr>
<tr>
<td width="40%"><a id=".pfm"></a><a id=".PFM"></a><dl>
<dt><b>.pfm</b></dt>
</dl>
</td>
<td width="60%">
Type 1 font metrics file. It is used with a .pfb file.

</td>
</tr>
</table>
 

To add a font whose information comes from several resource files, have <i>lpszFileName</i> point to a string with the file names separated by a "|" --for example, abcxxxxx.pfm | abcxxxxx.pfb.

## -returns

If the function succeeds, the return value specifies the number of fonts added.

If the function fails, the return value is zero. No extended error information is available.

## -remarks

Any application that adds or removes fonts from the system font table should notify other windows of the change by sending a <a href="/windows/desktop/gdi/wm-fontchange">WM_FONTCHANGE</a> message to all top-level windows in the operating system. The application should send this message by calling the <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> function and setting the <i>hwnd</i> parameter to HWND_BROADCAST.

When an application no longer needs a font resource that it loaded by calling the <b>AddFontResource</b> function, it must remove that resource by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourcea">RemoveFontResource</a> function.

This function installs the font only for the current session. When the system restarts, the font will not be present. To have the font installed even after restarting the system, the font must be listed in the registry.

A font listed in the registry and installed to a location other than the %windir%\fonts\ folder cannot be modified, deleted, or replaced as long as it is loaded in any session. In order to change one of these fonts, it must first be removed by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourcea">RemoveFontResource</a>, removed from the font registry (<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts</b>), and the system restarted. After restarting the system, the font will no longer be loaded and can be changed.





> [!NOTE]
> The wingdi.h header defines AddFontResource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourcea">RemoveFontResource
      </a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>
