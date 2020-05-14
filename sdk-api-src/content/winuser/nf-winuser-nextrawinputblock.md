---
UID: NF:winuser.NEXTRAWINPUTBLOCK
title: NEXTRAWINPUTBLOCK macro (winuser.h)
description: Retrieves the location of the next structure in an array of RAWINPUT structures.helpviewer_keywords: ["NEXTRAWINPUTBLOCK","NEXTRAWINPUTBLOCK macro [Keyboard and Mouse Input]","_win32_NEXTRAWINPUTBLOCK","_win32_nextrawinputblock_cpp","inputdev.nextrawinputblock","winui._win32_nextrawinputblock","winuser/NEXTRAWINPUTBLOCK"]
old-location: inputdev\nextrawinputblock.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputmacros\nextrawinputblock.htm
ms.date: 12/05/2018
ms.keywords: NEXTRAWINPUTBLOCK, NEXTRAWINPUTBLOCK macro [Keyboard and Mouse Input], _win32_NEXTRAWINPUTBLOCK, _win32_nextrawinputblock_cpp, inputdev.nextrawinputblock, winui._win32_nextrawinputblock, winuser/NEXTRAWINPUTBLOCK
f1_keywords:
- winuser/NEXTRAWINPUTBLOCK
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
- Winuser.h
api_name:
- NEXTRAWINPUTBLOCK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NEXTRAWINPUTBLOCK macro


## -description


Retrieves the location of the next structure in an array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures. 


## -parameters




### -param ptr

A pointer to a structure in an array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures. 


## -remarks



This macro is called repeatedly to traverse an array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structures.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
 

 

