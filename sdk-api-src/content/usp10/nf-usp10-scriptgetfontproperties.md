---
UID: NF:usp10.ScriptGetFontProperties
title: ScriptGetFontProperties function
author: windows-sdk-content
description: Retrieves information from the font cache on the special glyphs used by a font.
old-location: intl\scriptgetfontproperties.htm
tech.root: Intl
ms.assetid: eaad115c-4c1a-43e8-8dff-9d9640ef6ad7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ScriptGetFontProperties, ScriptGetFontProperties function [Internationalization for Windows Applications], _win32_ScriptGetFontProperties, intl.scriptgetfontproperties, usp10/ScriptGetFontProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetFontProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
---

# ScriptGetFontProperties function


## -description


Retrieves information from the font cache on the special glyphs used by a font.


## -parameters




### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>.


### -param psc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure identifying the script cache.


### -param sfp [out]

Pointer to a <a href="https://msdn.microsoft.com/6757e758-6525-47a4-9ed4-99ef42fa14a3">SCRIPT_FONTPROPERTIES</a> structure in which this function retrieves the information from the font cache.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



The structure retrieved by this function identifies the glyphs that are used for blanks, missing glyphs, invalid combinations, and the smallest kashida.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/6757e758-6525-47a4-9ed4-99ef42fa14a3">SCRIPT_FONTPROPERTIES</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

