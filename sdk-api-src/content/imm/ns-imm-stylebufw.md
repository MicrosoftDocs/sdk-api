---
UID: NS:imm.tagSTYLEBUFW
title: STYLEBUFW (imm.h)
author: windows-sdk-content
description: Contains the identifier and name of a style.
old-location: intl\stylebuf.htm
tech.root: Intl
ms.assetid: 72681071-58c4-490a-83d5-5013871ca875
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSTYLEBUFW, *NPSTYLEBUFW, *PSTYLEBUFW, PSTYLEBUF, PSTYLEBUF structure pointer [Internationalization for Windows Applications], STYLEBUF, STYLEBUF structure [Internationalization for Windows Applications], STYLEBUFA, STYLEBUFW, _win32_STYLEBUF_str, imm/PSTYLEBUF, imm/STYLEBUF, imm/STYLEBUFA, imm/STYLEBUFW, intl.stylebuf, tagSTYLEBUFA, tagSTYLEBUFW"
ms.topic: struct
f1_keywords: 
 - "imm/STYLEBUF"
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
targetos: Windows
req.typenames: STYLEBUFW, *PSTYLEBUFW, *NPSTYLEBUFW, *LPSTYLEBUFW
req.redist: 
ms.custom: 19H1
---

# STYLEBUFW structure


## -description



Contains the identifier and name of a style.




## -struct-fields




### -field dwStyle

Style of the register string. Can be IME_REGWORD_STYLE_EUDC to indicate a string in the EUDC range.


### -field szDescription

Description of the style.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
 

 

