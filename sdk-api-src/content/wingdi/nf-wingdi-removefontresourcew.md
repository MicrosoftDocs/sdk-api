---
UID: NF:wingdi.RemoveFontResourceW
title: RemoveFontResourceW function
author: windows-sdk-content
description: The RemoveFontResource function removes the fonts in the specified file from the system font table.
old-location: gdi\removefontresource.htm
tech.root: gdi
ms.assetid: ccc0ac8b-e373-47a9-a362-64fd79a33d0c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RemoveFontResource, RemoveFontResource function [Windows GDI], RemoveFontResourceA, RemoveFontResourceW, _win32_RemoveFontResource, gdi.removefontresource, wingdi/RemoveFontResource, wingdi/RemoveFontResourceA, wingdi/RemoveFontResourceW
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
req.unicode-ansi: RemoveFontResourceW (Unicode) and RemoveFontResourceA (ANSI)
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
 - RemoveFontResource
 - RemoveFontResourceA
 - RemoveFontResourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveFontResourceW function


## -description


The <b>RemoveFontResource</b> function removes the fonts in the specified file from the system font table.

If the font was added using the <a href="https://msdn.microsoft.com/eaf8ebf0-1b06-4a09-a842-83540245a117">AddFontResourceEx</a> function, you must use the <a href="https://msdn.microsoft.com/18056fe7-1efe-428e-a828-3217c53371eb">RemoveFontResourceEx</a> function.


## -parameters




### -param lpFileName [in]

A pointer to a null-terminated string that names a font resource file.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



We recommend that if an app adds or removes fonts from the system font table that it notify other windows of the change by sending a <a href="https://msdn.microsoft.com/4774308e-2f18-4a35-a769-56871f3c29a2">WM_FONTCHANGE</a> message to all top-level windows in the system. The app sends this message by calling the <a href="_win32_sendmessage_cpp">SendMessage</a> function with the <i>hwnd</i> parameter set to HWND_BROADCAST.

If there are outstanding references to a font, the associated resource remains loaded until no device context is using it. Furthermore, if the font is listed in the font registry (<b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts</b>) and is installed to any location other than the %windir%\fonts\ folder, it may be loaded into other active sessions (including session 0).

When you try to replace an existing font file that contains a font with outstanding references to it, you might get an error that indicates that the original font can't be deleted because it’s in use even after you call <b>RemoveFontResource</b>. If your app requires that the font file be replaced, to reduce the resource count of the original font to zero, call <b>RemoveFontResource</b> in a loop as shown in this example code. If you continue to get errors, this is an indication that the font file remains loaded in other sessions. Make sure the font isn't listed in the font registry and restart the system to ensure the font is unloaded from all sessions. 

<div class="alert"><b>Note</b>  Apps where the original font file is in use will still be able to access the original file and won't use the new font until the font reloads. Call <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> to reload the font.  We recommend that you call <b>AddFontResource</b> the same number of times as the call to <b>RemoveFontResource</b> succeeded as shown in this example code.</div>
<div> </div>
<pre class="syntax" xml:space="preserve"><code>
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
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/18056fe7-1efe-428e-a828-3217c53371eb">RemoveFontResourceEx</a>



<a href="_win32_sendmessage_cpp">SendMessage</a>
 

 

