---
UID: NS:richedit.tagHyphenateInfo
title: tagHyphenateInfo
author: windows-sdk-content
description: Contains information about hyphenation in a Microsoft Rich Edit control.
old-location: controls\HYPHENATEINFO.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphenateinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HYPHENATEINFO, HYPHENATEINFO structure [Windows Controls], _win32_HYPHENATEINFO_str, _win32_HYPHENATEINFO_str_cpp, controls.HYPHENATEINFO, controls._win32_HYPHENATEINFO_str, richedit/HYPHENATEINFO, tagHyphenateInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: HYPHENATEINFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagHyphenateInfo structure


## -description


Contains information about hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size of the <b>HYPHENATEINFO</b> structure, in bytes. 


### -field dxHyphenateZone

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size, in TWIPS (one TWIP is 1/1440 inch), of the area near the margin that excludes hyphenation. If a space character is closer to the margin than this value, do not hyphenate the following word. 


### -field pfnHyphenate

Type: <b>PFNHYPHENATEPROC</b>

The client-defined <a href="https://msdn.microsoft.com/en-us/library/Bb774370(v=VS.85).aspx">HyphenateProc</a> callback function. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb788033(v=VS.85).aspx">EM_GETHYPHENATEINFO</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774242(v=VS.85).aspx">EM_SETHYPHENATEINFO</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb788033(v=VS.85).aspx">EM_GETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774242(v=VS.85).aspx">EM_SETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774370(v=VS.85).aspx">HyphenateProc</a>



<b>Reference</b>
 

 

