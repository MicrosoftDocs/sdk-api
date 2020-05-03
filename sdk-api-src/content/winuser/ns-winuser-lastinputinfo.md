---
UID: NS:winuser.tagLASTINPUTINFO
title: LASTINPUTINFO (winuser.h)
description: Contains the time of the last input.helpviewer_keywords: ["*PLASTINPUTINFO","LASTINPUTINFO","LASTINPUTINFO structure [Keyboard and Mouse Input]","PLASTINPUTINFO","PLASTINPUTINFO structure pointer [Keyboard and Mouse Input]","_win32_LASTINPUTINFO_str","_win32_lastinputinfo_str_cpp","inputdev.lastinputinfo","winui._win32_lastinputinfo_str","winuser/LASTINPUTINFO","winuser/PLASTINPUTINFO"]
old-location: inputdev\lastinputinfo.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\lastinputinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PLASTINPUTINFO, LASTINPUTINFO, LASTINPUTINFO structure [Keyboard and Mouse Input], PLASTINPUTINFO, PLASTINPUTINFO structure pointer [Keyboard and Mouse Input], _win32_LASTINPUTINFO_str, _win32_lastinputinfo_str_cpp, inputdev.lastinputinfo, winui._win32_lastinputinfo_str, winuser/LASTINPUTINFO, winuser/PLASTINPUTINFO'
f1_keywords:
- winuser/LASTINPUTINFO
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- LASTINPUTINFO
targetos: Windows
req.typenames: LASTINPUTINFO, *PLASTINPUTINFO
req.redist: 
ms.custom: 19H1
---

# LASTINPUTINFO structure


## -description


Contains the time of the last input.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the structure, in bytes. This member must be set to <code>sizeof(LASTINPUTINFO)</code>. 


### -field dwTime

Type: <b>DWORD</b>

The tick count when the last input event was received. 


## -remarks



This function is useful for input idle detection. For more information on tick counts, see <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getlastinputinfo">GetLastInputInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>
 

 

