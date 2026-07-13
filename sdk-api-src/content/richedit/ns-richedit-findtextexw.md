---
UID: NS:richedit._findtextexw
title: FINDTEXTEXW (richedit.h)
description: Contains information about text to search for in a rich edit control. This structure is used with the EM_FINDTEXTEX message. (Unicode)
helpviewer_keywords: ["FINDTEXTEX","FINDTEXTEX structure [Windows Controls]","FINDTEXTEXA","FINDTEXTEXW","_win32_FINDTEXTEX_str","_win32_FINDTEXTEX_str_cpp","controls.FINDTEXTEX","controls._win32_FINDTEXTEX_str","richedit/FINDTEXTEX","richedit/FINDTEXTEXA","richedit/FINDTEXTEXW"]
old-location: controls\FINDTEXTEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtextex.htm
ms.date: 12/05/2018
ms.keywords: FINDTEXTEX, FINDTEXTEX structure [Windows Controls], FINDTEXTEXA, FINDTEXTEXW, _win32_FINDTEXTEX_str, _win32_FINDTEXTEX_str_cpp, controls.FINDTEXTEX, controls._win32_FINDTEXTEX_str, richedit/FINDTEXTEX, richedit/FINDTEXTEXA, richedit/FINDTEXTEXW
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FINDTEXTEXW (Unicode) and FINDTEXTEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FINDTEXTEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _findtextexw
 - richedit/_findtextexw
 - FINDTEXTEXW
 - richedit/FINDTEXTEXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - FINDTEXTEX
 - FINDTEXTEXA
 - FINDTEXTEXW
---

# FINDTEXTEXW structure


## -description

Contains information about text to search for in a rich edit control. This structure is used with the <a href="/windows/win32/controls/em-findtextex">EM_FINDTEXTEX</a> message.

## -struct-fields

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of characters to search. To search forward in the entire control, set <b>cpMin</b> to 0 and <b>cpMax</b> to -1.

### -field lpstrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The null-terminated string to find.

### -field chrgText

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of characters in which the text was found. If the text was not found, <b>cpMin</b> and <b>cpMax</b> are -1.

## -see-also

<a href="/windows/win32/controls/em-findtextex">EM_FINDTEXTEX</a>



<a href="/windows/win32/controls/em-findtextexw">EM_FINDTEXTEXW</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The richedit.h header defines FINDTEXTEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
