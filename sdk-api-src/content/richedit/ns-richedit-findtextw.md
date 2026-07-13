---
UID: NS:richedit._findtextw
title: FINDTEXTW (richedit.h)
description: Contains information about a search operation in a rich edit control. This structure is used with the EM_FINDTEXT message. (Unicode)
helpviewer_keywords: ["FINDTEXT","FINDTEXT structure [Windows Controls]","FINDTEXTA","FINDTEXTW","_win32_FINDTEXT_str","_win32_FINDTEXT_str_cpp","controls.FINDTEXT","controls._win32_FINDTEXT_str","richedit/FINDTEXT","richedit/FINDTEXTA","richedit/FINDTEXTW"]
old-location: controls\FINDTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtext.htm
ms.date: 12/05/2018
ms.keywords: FINDTEXT, FINDTEXT structure [Windows Controls], FINDTEXTA, FINDTEXTW, _win32_FINDTEXT_str, _win32_FINDTEXT_str_cpp, controls.FINDTEXT, controls._win32_FINDTEXT_str, richedit/FINDTEXT, richedit/FINDTEXTA, richedit/FINDTEXTW
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FINDTEXTW (Unicode) and FINDTEXTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FINDTEXTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _findtextw
 - richedit/_findtextw
 - FINDTEXTW
 - richedit/FINDTEXTW
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
 - FINDTEXT
 - FINDTEXTA
 - FINDTEXTW
---

# FINDTEXTW structure


## -description

Contains information about a search operation in a rich edit control. This structure is used with the <a href="/windows/win32/controls/em-findtext">EM_FINDTEXT</a> message.

## -struct-fields

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of characters to search.

### -field lpstrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The null-terminated string used in the find operation.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a>



<a href="/windows/win32/controls/em-findtext">EM_FINDTEXT</a>



<a href="/windows/win32/controls/em-findtextw">EM_FINDTEXTW</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The richedit.h header defines FINDTEXT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
