---
UID: NS:richedit.hyphresult
title: HYPHRESULT (richedit.h)
description: Contains information about the result of hyphenation in a Microsoft Rich Edit control.helpviewer_keywords: ["HYPHRESULT","HYPHRESULT structure [Windows Controls]","_win32_HYPHRESULT_str","_win32_HYPHRESULT_str_cpp","controls.HYPHRESULT","controls._win32_HYPHRESULT_str","richedit/HYPHRESULT"]
old-location: controls\HYPHRESULT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphresult.htm
ms.date: 12/05/2018
ms.keywords: HYPHRESULT, HYPHRESULT structure [Windows Controls], _win32_HYPHRESULT_str, _win32_HYPHRESULT_str_cpp, controls.HYPHRESULT, controls._win32_HYPHRESULT_str, richedit/HYPHRESULT
f1_keywords:
- richedit/HYPHRESULT
dev_langs:
- c++
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Richedit.h
api_name:
- HYPHRESULT
targetos: Windows
req.typenames: HYPHRESULT
req.redist: 
ms.custom: 19H1
---

# HYPHRESULT structure


## -description


Contains information about the result of hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field khyph

Type: <b><a href="https://msdn.microsoft.com/900cae36-d2e3-4a30-97ca-1cc832fd2687">KHYPH</a></b>

The type of hyphenation. 


### -field ichHyph

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The index of the WCHAR in the passed string where hyphenation occurred. 


### -field chHyph

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">WCHAR</a></b>

The character used when hyphenation requires a replacement or an addition or a change. If no new character is needed, the value is zero. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/2463189e-98cf-4545-a435-474df74e1a22">HYPHENATEINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/2463189e-98cf-4545-a435-474df74e1a22">HYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/900cae36-d2e3-4a30-97ca-1cc832fd2687">KHYPH</a>



<b>Reference</b>
 

 

