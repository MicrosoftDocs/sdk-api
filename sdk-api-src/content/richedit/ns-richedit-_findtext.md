---
UID: NS:richedit._findtext
title: "_findtext"
author: windows-sdk-content
description: Contains information about a search operation in a rich edit control. This structure is used with the EM_FINDTEXT message.
old-location: controls\FINDTEXT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\findtext.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: FINDTEXT, FINDTEXT structure [Windows Controls], FINDTEXTA, FINDTEXTW, _findtext, _win32_FINDTEXT_str, _win32_FINDTEXT_str_cpp, controls.FINDTEXT, controls._win32_FINDTEXT_str, richedit/FINDTEXT, richedit/FINDTEXTA, richedit/FINDTEXTW
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
product: Windows
targetos: Windows
req.typenames: FINDTEXTA
req.redist: 
---

# _findtext structure


## -description


Contains information about a search operation in a rich edit control. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb788009(v=VS.85).aspx">EM_FINDTEXT</a> message.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a></b>

The range of characters to search. 


### -field lpstrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The null-terminated string used in the find operation. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb788009(v=VS.85).aspx">EM_FINDTEXT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb788015(v=VS.85).aspx">EM_FINDTEXTW</a>



<b>Reference</b>
 

 

