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

# tag_SCRIPT_JUSTIFY enumeration


## -description


Defines glyph characteristic information that an application needs to implement justification.


## -enum-fields




### -field SCRIPT_JUSTIFY_NONE

Justification cannot be applied at the glyph.


### -field SCRIPT_JUSTIFY_ARABIC_BLANK

The glyph represents a blank in an Arabic run.


### -field SCRIPT_JUSTIFY_CHARACTER

An inter-character justification point follows the glyph.


### -field SCRIPT_JUSTIFY_RESERVED1

Reserved.


### -field SCRIPT_JUSTIFY_BLANK

The glyph represents a blank outside an Arabic run.


### -field SCRIPT_JUSTIFY_RESERVED2

Reserved.


### -field SCRIPT_JUSTIFY_RESERVED3

Reserved.


### -field SCRIPT_JUSTIFY_ARABIC_NORMAL

Normal middle-of-word glyph that connects to the right (begin).


### -field SCRIPT_JUSTIFY_ARABIC_KASHIDA

Kashida (U+0640) in the middle of the word.


### -field SCRIPT_JUSTIFY_ARABIC_ALEF

Final form of an alef-like (U+0627, U+0625, U+0623, U+0622).


### -field SCRIPT_JUSTIFY_ARABIC_HA

Final form of Ha (U+0647).


### -field SCRIPT_JUSTIFY_ARABIC_RA

Final form of Ra (U+0631).


### -field SCRIPT_JUSTIFY_ARABIC_BA

Final form of Ba (U+0628).


### -field SCRIPT_JUSTIFY_ARABIC_BARA

Ligature of alike (U+0628,U+0631).


### -field SCRIPT_JUSTIFY_ARABIC_SEEN

Highest priority: initial shape of Seen class (U+0633).


### -field SCRIPT_JUSTIFY_ARABIC_SEEN_M

Highest priority: medial shape of Seen class (U+0633).


## -see-also




<a href="https://msdn.microsoft.com/83b77f60-2520-49ee-bc7f-27cb3db02ac8">SCRIPT_VISATTR</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/e2f4e7ee-ee46-4daa-a599-c5da9d133ccf">Uniscribe Enumeration Types</a>
 

 

