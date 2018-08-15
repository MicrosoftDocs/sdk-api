---
UID: NS:usp10.tagGOFFSET
title: tagGOFFSET
author: windows-sdk-content
description: Contains the x and y offsets of the combining glyph.
old-location: intl\goffset.htm
old-project: Intl
ms.assetid: 63fa8741-c8c8-480d-9702-2f4eb13bc01c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GOFFSET, GOFFSET structure [Internationalization for Windows Applications], _win32_GOFFSET_str, intl.goffset, tagGOFFSET, usp10/GOFFSET
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: usp10.h
req.include-header: 
req.redist: Internet Explorer 5 or later onWindows Me/98/95
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
req.typenames: GOFFSET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - GOFFSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tagGOFFSET structure


## -description



Contains the x and y offsets of the combining glyph.




## -struct-fields




### -field du

x offset, in logical units, for the combining glyph.


### -field dv

y offset, in logical units, for the combining glyph.


## -remarks



The members of this structure are named as they are so that they are not confused with the "dx" and "dy" designators for physical units in Uniscribe functions and structures.




## -see-also




<a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>



<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/8dc776a9-fdde-4982-a2ca-e4384615bc47">ScriptPositionSingleGlyph</a>



<a href="https://msdn.microsoft.com/8d69caeb-4c02-4a9f-9dd5-ac3c13561a57">ScriptTextOut</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

