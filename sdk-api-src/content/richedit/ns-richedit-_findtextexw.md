---
UID: NS:richedit._findtextexw
title: "_findtextexw"
author: windows-sdk-content
description: Contains information about text to search for in a rich edit control. This structure is used with the EM_FINDTEXTEX message.
old-location: controls\FINDTEXTEX.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtextex.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FINDTEXTEX, FINDTEXTEX structure [Windows Controls], FINDTEXTEXA, FINDTEXTEXW, _findtextexw, _win32_FINDTEXTEX_str, _win32_FINDTEXTEX_str_cpp, controls.FINDTEXTEX, controls._win32_FINDTEXTEX_str, richedit/FINDTEXTEX, richedit/FINDTEXTEXA, richedit/FINDTEXTEXW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: FINDTEXTEXW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _findtextexw structure


## -description


Contains information about text to search for in a rich edit control. This structure is used with the <a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a> message.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to search. To search forward in the entire control, set <b>cpMin</b> to 0 and <b>cpMax</b> to -1. 


### -field lpstrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The null-terminated string to find. 


### -field chrgText

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters in which the text was found. If the text was not found, <b>cpMin</b> and <b>cpMax</b> are -1.


## -see-also




<a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a>



<a href="https://msdn.microsoft.com/7b90ef06-0395-430e-8b5d-b392481a5f70">EM_FINDTEXTEXW</a>



<b>Reference</b>
 

 

