---
UID: NS:wingdi._ABC
title: ABC (wingdi.h)
author: windows-sdk-content
description: The ABC structure contains the width of a character in a TrueType font.
old-location: gdi\abc.htm
tech.root: gdi
ms.assetid: 00000000-0000-0000-0000-000000000001
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPABC, *NPABC, *PABC, ABC, ABC structure [Windows GDI], PABC, PABC structure pointer [Windows GDI], _win32_ABC_str, gdi.abc, wingdi/ABC, wingdi/PABC"
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - ABC
product: Windows
targetos: Windows
req.typenames: ABC, *PABC, *NPABC, *LPABC
req.redist: 
---

# ABC structure


## -description



The <b>ABC</b> structure contains the width of a character in a TrueType font.




## -struct-fields




### -field abcA

The A spacing of the character. The A spacing is the distance to add to the current position before drawing the character glyph.


### -field abcB

The B spacing of the character. The B spacing is the width of the drawn portion of the character glyph.


### -field abcC

The C spacing of the character. The C spacing is the distance to add to the current position to provide white space to the right of the character glyph.


## -remarks



The total width of a character is the summation of the A, B, and C spaces. Either the A or the C space can be negative to indicate underhangs or overhangs.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>
 

 

