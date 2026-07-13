---
UID: NF:wingdi.RemoveFontResourceExA
title: RemoveFontResourceExA function (wingdi.h)
description: The RemoveFontResourceEx function removes the fonts in the specified file from the system font table. (ANSI)
helpviewer_keywords: ["RemoveFontResourceExA", "wingdi/RemoveFontResourceExA"]
old-location: gdi\removefontresourceex.htm
tech.root: gdi
ms.assetid: 18056fe7-1efe-428e-a828-3217c53371eb
ms.date: 12/05/2018
ms.keywords: RemoveFontResourceEx, RemoveFontResourceEx function [Windows GDI], RemoveFontResourceExA, RemoveFontResourceExW, _win32_RemoveFontResourceEx, gdi.removefontresourceex, wingdi/RemoveFontResourceEx, wingdi/RemoveFontResourceExA, wingdi/RemoveFontResourceExW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveFontResourceExW (Unicode) and RemoveFontResourceExA (ANSI)
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
 - RemoveFontResourceExA
 - wingdi/RemoveFontResourceExA
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
 - RemoveFontResourceEx
 - RemoveFontResourceExA
 - RemoveFontResourceExW
---

# RemoveFontResourceExA function


## -description

The <b>RemoveFontResourceEx</b> function removes the fonts in the specified file from the system font table.

## -parameters

### -param name [in]

A pointer to a null-terminated string that names a font resource file.

### -param fl [in]

The characteristics of the font to be removed from the system. In order for the font to be removed, the flags used must be the same as when the font was added with the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a> function. See the <b>AddFontResourceEx</b> function for more information.

### -param pdv [in]

Reserved. Must be zero.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. No extended error information is available.

## -remarks

This function will only remove the font if the flags specified are the same as when then font was added with the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a> function.

When you try to replace an existing font file that contains a font with outstanding references to it, you might get an error that indicates that the original font can't be deleted because it’s in use even after you call <b>RemoveFontResourceEx</b>. If your app requires that the font file be replaced, to reduce the resource count of the original font to zero, call <b>RemoveFontResourceEx</b> in a loop as shown in this example code. If you continue to get errors, this is an indication that the font file remains loaded in other sessions. Make sure the font isn't listed in the font registry and restart the system to ensure the font is unloaded from all sessions.

<div class="alert"><b>Note</b>  Apps where the original font file is in use will still be able to access the original file and won't use the new font until the font reloads. Call <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a> to reload the font.  We recommend that you call <b>AddFontResourceEx</b> the same number of times as the call to <b>RemoveFontResourceEx</b> succeeded as shown in this example code.</div>
<div> </div>

``` syntax

int i = 0;
while( RemoveFontResourceEx( FontFile, FR_PRIVATE, 0 ) )
{
    i++;
}

// TODO: Replace font file

while( i-- )
{
    AddFontResourceEx( FontFile, FR_PRIVATE, 0 );
}

```





> [!NOTE]
> The wingdi.h header defines RemoveFontResourceEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>
