---
UID: NF:wingdi.RemoveFontResourceA
title: RemoveFontResourceA function (wingdi.h)
description: The RemoveFontResource function removes the fonts in the specified file from the system font table. (ANSI)
helpviewer_keywords: ["RemoveFontResourceA", "wingdi/RemoveFontResourceA"]
old-location: gdi\removefontresource.htm
tech.root: gdi
ms.assetid: ccc0ac8b-e373-47a9-a362-64fd79a33d0c
ms.date: 12/05/2018
ms.keywords: RemoveFontResource, RemoveFontResource function [Windows GDI], RemoveFontResourceA, RemoveFontResourceW, _win32_RemoveFontResource, gdi.removefontresource, wingdi/RemoveFontResource, wingdi/RemoveFontResourceA, wingdi/RemoveFontResourceW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveFontResourceW (Unicode) and RemoveFontResourceA (ANSI)
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
 - RemoveFontResourceA
 - wingdi/RemoveFontResourceA
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
 - RemoveFontResource
 - RemoveFontResourceA
 - RemoveFontResourceW
---

# RemoveFontResourceA function


## -description

The <b>RemoveFontResource</b> function removes the fonts in the specified file from the system font table.

If the font was added using the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a> function, you must use the <a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourceexa">RemoveFontResourceEx</a> function.

## -parameters

### -param lpFileName [in]

A pointer to a null-terminated string that names a font resource file.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

We recommend that if an app adds or removes fonts from the system font table that it notify other windows of the change by sending a <a href="/windows/desktop/gdi/wm-fontchange">WM_FONTCHANGE</a> message to all top-level windows in the system. The app sends this message by calling the <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> function with the <i>hwnd</i> parameter set to HWND_BROADCAST.

If there are outstanding references to a font, the associated resource remains loaded until no device context is using it. Furthermore, if the font is listed in the font registry (<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts</b>) and is installed to any location other than the %windir%\fonts\ folder, it may be loaded into other active sessions (including session 0).

When you try to replace an existing font file that contains a font with outstanding references to it, you might get an error that indicates that the original font can't be deleted because it’s in use even after you call <b>RemoveFontResource</b>. If your app requires that the font file be replaced, to reduce the resource count of the original font to zero, call <b>RemoveFontResource</b> in a loop as shown in this example code. If you continue to get errors, this is an indication that the font file remains loaded in other sessions. Make sure the font isn't listed in the font registry and restart the system to ensure the font is unloaded from all sessions. 

<div class="alert"><b>Note</b>  Apps where the original font file is in use will still be able to access the original file and won't use the new font until the font reloads. Call <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> to reload the font.  We recommend that you call <b>AddFontResource</b> the same number of times as the call to <b>RemoveFontResource</b> succeeded as shown in this example code.</div>
<div> </div>

``` syntax

int i = 0;
while( RemoveFontResource( FontFile ) )
{
    i++;
}

// TODO: Replace font file

while( i-- )
{
    AddFontResource( FontFile );
}

```





> [!NOTE]
> The wingdi.h header defines RemoveFontResource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourceexa">RemoveFontResourceEx</a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>
