---
UID: NS:immdev.tagREGISTERWORDA
title: REGISTERWORDA (immdev.h)
description: The REGISTERWORDA (ANSI) structure (immdev.h) contains reading information or a word to register. 
helpviewer_keywords: ["*LPREGISTERWORDA","*NPREGISTERWORDA","*PREGISTERWORDA","PREGISTERWORD","PREGISTERWORD structure pointer [Internationalization for Windows Applications]","REGISTERWORD","REGISTERWORD structure [Internationalization for Windows Applications]","REGISTERWORDA","REGISTERWORDW","_win32_REGISTERWORD_str","imm/PREGISTERWORD","imm/REGISTERWORD","imm/REGISTERWORDA","imm/REGISTERWORDW","intl.registerword","tagREGISTERWORDA","tagREGISTERWORDW"]
old-location: intl\registerword.htm
tech.root: Intl
ms.assetid: 70a11a96-a0e3-4741-be91-b85eb38cd767
ms.date: 08/05/2022
ms.keywords: '*LPREGISTERWORDA, *NPREGISTERWORDA, *PREGISTERWORDA, PREGISTERWORD, PREGISTERWORD structure pointer [Internationalization for Windows Applications], REGISTERWORD, REGISTERWORD structure [Internationalization for Windows Applications], REGISTERWORDA, REGISTERWORDW, _win32_REGISTERWORD_str, imm/PREGISTERWORD, imm/REGISTERWORD, imm/REGISTERWORDA, imm/REGISTERWORDW, intl.registerword, tagREGISTERWORDA, tagREGISTERWORDW'
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: REGISTERWORDW (Unicode) and REGISTERWORDA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REGISTERWORDA, *PREGISTERWORDA, *NPREGISTERWORDA, *LPREGISTERWORDA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREGISTERWORDA
 - immdev/tagREGISTERWORDA
 - PREGISTERWORDA
 - immdev/PREGISTERWORDA
 - REGISTERWORDA
 - immdev/REGISTERWORDA
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
 - REGISTERWORD
 - REGISTERWORDA
 - REGISTERWORDW
---

# REGISTERWORDA structure


## -description

Contains reading information or a word to register.

## -struct-fields

### -field lpReading

Pointer to the reading information for the word to register. If the reading information is not needed, the member can be set to <b>NULL</b>.

### -field lpWord

Pointer to the word to register. If a word is not needed, the member can be set to <b>NULL</b>.

## -remarks

The application can pass this structure to the <a href="/windows/desktop/api/imm/nf-imm-immconfigureimea">ImmConfigureIME</a> function to have the information or word appear as an initial value in the configuration dialog box for the IME.





> [!NOTE]
> The immdev.h header defines REGISTERWORD as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immconfigureimea">ImmConfigureIME</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
