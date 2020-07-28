---
UID: NS:richedit._findtext
title: FINDTEXTA (richedit.h)
description: Contains information about a search operation in a rich edit control. This structure is used with the EM_FINDTEXT message.
helpviewer_keywords: ["FINDTEXT","FINDTEXT structure [Windows Controls]","FINDTEXTA","FINDTEXTW","_win32_FINDTEXT_str","_win32_FINDTEXT_str_cpp","controls.FINDTEXT","controls._win32_FINDTEXT_str","richedit/FINDTEXT","richedit/FINDTEXTA","richedit/FINDTEXTW"]
old-location: controls\FINDTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtext.htm
ms.date: 12/05/2018
ms.keywords: FINDTEXT, FINDTEXT structure [Windows Controls], FINDTEXTA, FINDTEXTW, _win32_FINDTEXT_str, _win32_FINDTEXT_str_cpp, controls.FINDTEXT, controls._win32_FINDTEXT_str, richedit/FINDTEXT, richedit/FINDTEXTA, richedit/FINDTEXTW
f1_keywords:
- richedit/FINDTEXT
dev_langs:
- c++
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
targetos: Windows
req.typenames: FINDTEXTA
req.redist: 
ms.custom: 19H1
---

# FINDTEXTA structure


## -description


Contains information about a search operation in a rich edit control. This structure is used with the <a href="https://msdn.microsoft.com/f19e19a0-d8dd-4d31-b76d-f1f09577dd2d">EM_FINDTEXT</a> message.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to search. 


### -field lpstrText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The null-terminated string used in the find operation. 


## -see-also




<a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>



<a href="https://msdn.microsoft.com/f19e19a0-d8dd-4d31-b76d-f1f09577dd2d">EM_FINDTEXT</a>



<a href="https://msdn.microsoft.com/0c1579f5-3b37-4e28-86a2-f4e03e195f38">EM_FINDTEXTW</a>



<b>Reference</b>
 

 

## -remarks

> [!NOTE]
> The richedit.h header defines FINDTEXT as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

