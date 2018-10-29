---
UID: NS:imm.tagSTYLEBUFW
title: tagSTYLEBUFW
author: windows-sdk-content
description: Contains the identifier and name of a style.
old-location: intl\stylebuf.htm
tech.root: Intl
ms.assetid: 72681071-58c4-490a-83d5-5013871ca875
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPSTYLEBUFW, *NPSTYLEBUFW, *PSTYLEBUFW, PSTYLEBUF, PSTYLEBUF structure pointer [Internationalization for Windows Applications], STYLEBUF, STYLEBUF structure [Internationalization for Windows Applications], STYLEBUFA, STYLEBUFW, _win32_STYLEBUF_str, imm/PSTYLEBUF, imm/STYLEBUF, imm/STYLEBUFA, imm/STYLEBUFW, intl.stylebuf, tagSTYLEBUFA, tagSTYLEBUFW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: STYLEBUFW (Unicode) and STYLEBUFA (ANSI)
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
 - Imm.h
api_name:
 - STYLEBUF
 - STYLEBUFA
 - STYLEBUFW
product: Windows
targetos: Windows
req.typenames: STYLEBUFW, *PSTYLEBUFW, *NPSTYLEBUFW, *LPSTYLEBUFW
req.redist: 
---

# tagSTYLEBUFW structure


## -description



Contains the identifier and name of a style.




## -struct-fields




### -field dwStyle

Style of the register string. Can be IME_REGWORD_STYLE_EUDC to indicate a string in the EUDC range.


### -field szDescription

Description of the style.


## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

