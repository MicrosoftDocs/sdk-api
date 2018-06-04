---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

