---
UID: NS:richedit._findtextexa
title: FINDTEXTEXA (richedit.h)
description: Contains information about text to search for in a rich edit control. This structure is used with the EM_FINDTEXTEX message.helpviewer_keywords: ["FINDTEXTEX","FINDTEXTEX structure [Windows Controls]","FINDTEXTEXA","FINDTEXTEXW","_win32_FINDTEXTEX_str","_win32_FINDTEXTEX_str_cpp","controls.FINDTEXTEX","controls._win32_FINDTEXTEX_str","richedit/FINDTEXTEX","richedit/FINDTEXTEXA","richedit/FINDTEXTEXW"]
old-location: controls\FINDTEXTEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtextex.htm
ms.date: 12/05/2018
ms.keywords: FINDTEXTEX, FINDTEXTEX structure [Windows Controls], FINDTEXTEXA, FINDTEXTEXW, _win32_FINDTEXTEX_str, _win32_FINDTEXTEX_str_cpp, controls.FINDTEXTEX, controls._win32_FINDTEXTEX_str, richedit/FINDTEXTEX, richedit/FINDTEXTEXA, richedit/FINDTEXTEXW
f1_keywords:
- richedit/FINDTEXTEX
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
req.unicode-ansi: FINDTEXTEXW (Unicode) and FINDTEXTEXA (ANSI)
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
- FINDTEXTEX
- FINDTEXTEXA
- FINDTEXTEXW
targetos: Windows
req.typenames: FINDTEXTEXA
req.redist: 
ms.custom: 19H1
---

# FINDTEXTEXA structure


## -description


Contains information about text to search for in a rich edit control. This structure is used with the <a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a> message.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to search. To search forward in the entire control, set <b>cpMin</b> to 0 and <b>cpMax</b> to -1. 


### -field lpstrText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The null-terminated string to find. 


### -field chrgText

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters in which the text was found. If the text was not found, <b>cpMin</b> and <b>cpMax</b> are -1.


## -see-also




<a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a>



<a href="https://msdn.microsoft.com/7b90ef06-0395-430e-8b5d-b392481a5f70">EM_FINDTEXTEXW</a>



<b>Reference</b>
 

 

