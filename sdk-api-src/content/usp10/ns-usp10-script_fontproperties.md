---
UID: NS:usp10.SCRIPT_FONTPROPERTIES
title: SCRIPT_FONTPROPERTIES
author: windows-sdk-content
description: Contains information about the properties of the current font.
old-location: intl\script_fontproperties.htm
old-project: Intl
ms.assetid: 6757e758-6525-47a4-9ed4-99ef42fa14a3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SCRIPT_FONTPROPERTIES, SCRIPT_FONTPROPERTIES structure [Internationalization for Windows Applications], _win32_SCRIPT_FONTPROPERTIES_str, intl.script_fontproperties, usp10/SCRIPT_FONTPROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SCRIPT_FONTPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usp10.h
api_name:
-	SCRIPT_FONTPROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# SCRIPT_FONTPROPERTIES structure


## -description



Contains information about the properties of the current font.




## -struct-fields




### -field cBytes

Size, in bytes, of the structure.


### -field wgBlank

Glyph used to indicate a blank.


### -field wgDefault

Glyph used to indicate Unicode characters not present in the font.


### -field wgInvalid

Glyph used to indicate invalid character combinations.


### -field wgKashida

Glyph used to indicate the shortest continuous kashida, with 1 indicating that the font contains no kashida.


### -field iKashidaWidth

Width of the shortest continuous kashida glyph in the font, indicated by the <b>wgKashida</b> member.


## -see-also




<a href="https://msdn.microsoft.com/eaad115c-4c1a-43e8-8dff-9d9640ef6ad7">ScriptGetFontProperties</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

