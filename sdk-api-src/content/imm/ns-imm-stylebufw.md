---
UID: NS:imm.tagSTYLEBUFW
title: STYLEBUFW (imm.h)
description: Contains the identifier and name of a style.
helpviewer_keywords: ["*LPSTYLEBUFW","*NPSTYLEBUFW","*PSTYLEBUFW","PSTYLEBUF","PSTYLEBUF structure pointer [Internationalization for Windows Applications]","STYLEBUF","STYLEBUF structure [Internationalization for Windows Applications]","STYLEBUFA","STYLEBUFW","_win32_STYLEBUF_str","imm/PSTYLEBUF","imm/STYLEBUF","imm/STYLEBUFA","imm/STYLEBUFW","intl.stylebuf","tagSTYLEBUFA","tagSTYLEBUFW"]
old-location: intl\stylebuf.htm
tech.root: Intl
ms.assetid: 72681071-58c4-490a-83d5-5013871ca875
ms.date: 12/05/2018
ms.keywords: '*LPSTYLEBUFW, *NPSTYLEBUFW, *PSTYLEBUFW, PSTYLEBUF, PSTYLEBUF structure pointer [Internationalization for Windows Applications], STYLEBUF, STYLEBUF structure [Internationalization for Windows Applications], STYLEBUFA, STYLEBUFW, _win32_STYLEBUF_str, imm/PSTYLEBUF, imm/STYLEBUF, imm/STYLEBUFA, imm/STYLEBUFW, intl.stylebuf, tagSTYLEBUFA, tagSTYLEBUFW'
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
targetos: Windows
req.typenames: STYLEBUFW, *PSTYLEBUFW, *NPSTYLEBUFW, *LPSTYLEBUFW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTYLEBUFW
 - imm/tagSTYLEBUFW
 - PSTYLEBUFW
 - imm/PSTYLEBUFW
 - STYLEBUFW
 - imm/STYLEBUFW
dev_langs:
 - c++
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

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>

## -remarks

> [!NOTE]
> The imm.h header defines STYLEBUF as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).