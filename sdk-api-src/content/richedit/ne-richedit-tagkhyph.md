---
UID: NE:richedit.tagKHYPH
title: tagKHYPH
author: windows-sdk-content
description: Contains values used to specify how to do hyphenation in a rich edit control. The HyphenateProc callback function uses this enumeration type.
old-location: controls\KHYPH.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditenumerationtypes\khyph.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: KHYPH, KHYPH enumeration [Windows Controls], _win32_KHYPH, _win32_KHYPH_cpp, controls.KHYPH, controls._win32_KHYPH, khyphAddBefore, khyphChangeAfter, khyphChangeBefore, khyphDelAndChange, khyphDeleteBefore, khyphNil, khyphNormal, richedit/KHYPH, richedit/khyphAddBefore, richedit/khyphChangeAfter, richedit/khyphChangeBefore, richedit/khyphDelAndChange, richedit/khyphDeleteBefore, richedit/khyphNil, richedit/khyphNormal, tagKHYPH
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: KHYPH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - KHYPH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagKHYPH enumeration


## -description


Contains values used to specify how to do hyphenation in a rich edit control. The <a href="https://msdn.microsoft.com/en-us/library/Bb774370(v=VS.85).aspx">HyphenateProc</a> callback function uses this enumeration type. 


## -enum-fields




### -field khyphNil

No hyphenation is allowed. 


### -field khyphNormal

Do not change any characters during hyphenation.


### -field khyphAddBefore

Add a letter before the hyphenation mark. 


### -field khyphChangeBefore

Change the letter before the hyphenation mark. 


### -field khyphDeleteBefore

Delete the letter before the hyphenation mark. 


### -field khyphChangeAfter

Change the letter after the hyphenation mark. 


### -field khyphDelAndChange

The two letters before the hyphenation mark are replaced by one character; see the <b>chHyph</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb787932(v=VS.85).aspx">HYPHRESULT</a>.


## -remarks



Hyphenation rules are specific for each language; not all hyphenation types are valid for a given language.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787932(v=VS.85).aspx">HYPHRESULT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774370(v=VS.85).aspx">HyphenateProc</a>



<b>Reference</b>
 

 

