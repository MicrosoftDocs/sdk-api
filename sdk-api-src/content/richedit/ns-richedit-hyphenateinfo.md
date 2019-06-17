---
UID: NS:richedit.tagHyphenateInfo
title: HYPHENATEINFO (richedit.h)
author: windows-sdk-content
description: Contains information about hyphenation in a Microsoft Rich Edit control.
old-location: controls\HYPHENATEINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphenateinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HYPHENATEINFO, HYPHENATEINFO structure [Windows Controls], _win32_HYPHENATEINFO_str, _win32_HYPHENATEINFO_str_cpp, controls.HYPHENATEINFO, controls._win32_HYPHENATEINFO_str, richedit/HYPHENATEINFO
ms.topic: struct
f1_keywords: ["richedit/HYPHENATEINFO"]
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
 - HYPHENATEINFO
product: Windows
targetos: Windows
req.typenames: HYPHENATEINFO
req.redist: 
ms.custom: 19H1
---

# HYPHENATEINFO structure


## -description


Contains information about hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field cbSize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size of the <b>HYPHENATEINFO</b> structure, in bytes. 


### -field dxHyphenateZone

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size, in TWIPS (one TWIP is 1/1440 inch), of the area near the margin that excludes hyphenation. If a space character is closer to the margin than this value, do not hyphenate the following word. 


### -field pfnHyphenate

Type: <b>PFNHYPHENATEPROC</b>

The client-defined <a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a> callback function. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/70ccb698-e440-493b-8f38-2bf7f32e4b26">EM_GETHYPHENATEINFO</a> and <a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/70ccb698-e440-493b-8f38-2bf7f32e4b26">EM_GETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a>



<b>Reference</b>
 

 

