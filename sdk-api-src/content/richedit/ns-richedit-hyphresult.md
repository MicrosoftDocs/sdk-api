---
UID: NS:richedit.hyphresult
title: hyphresult
author: windows-sdk-content
description: Contains information about the result of hyphenation in a Microsoft Rich Edit control.
old-location: controls\HYPHRESULT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphresult.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HYPHRESULT, HYPHRESULT structure [Windows Controls], _win32_HYPHRESULT_str, _win32_HYPHRESULT_str_cpp, controls.HYPHRESULT, controls._win32_HYPHRESULT_str, hyphresult, richedit/HYPHRESULT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: HYPHRESULT
req.redist: 
---

# hyphresult structure


## -description


Contains information about the result of hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field khyph

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774363(v=VS.85).aspx">KHYPH</a></b>

The type of hyphenation. 


### -field ichHyph

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The index of the WCHAR in the passed string where hyphenation occurred. 


### -field chHyph

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a></b>

The character used when hyphenation requires a replacement or an addition or a change. If no new character is needed, the value is zero. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb787930(v=VS.85).aspx">HYPHENATEINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787930(v=VS.85).aspx">HYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774363(v=VS.85).aspx">KHYPH</a>



<b>Reference</b>
 

 

