---
UID: NS:winuser.tagCWPSTRUCT
title: tagCWPSTRUCT
author: windows-sdk-content
description: Defines the message parameters passed to a WH_CALLWNDPROC hook procedure, CallWndProc.
old-location: winmsg\cwpstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cwpstruct.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPCWPSTRUCT, *NPCWPSTRUCT, *PCWPSTRUCT, CWPSTRUCT, CWPSTRUCT structure [Windows and Messages], LPCWPSTRUCT, LPCWPSTRUCT structure pointer [Windows and Messages], PCWPSTRUCT, PCWPSTRUCT structure pointer [Windows and Messages], _win32_CWPSTRUCT_str, _win32_cwpstruct_str_cpp, tagCWPSTRUCT, winmsg.cwpstruct, winui._win32_cwpstruct_str, winuser/CWPSTRUCT, winuser/LPCWPSTRUCT, winuser/PCWPSTRUCT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - CWPSTRUCT
product: Windows
targetos: Windows
req.typenames: CWPSTRUCT, *PCWPSTRUCT, *NPCWPSTRUCT, *LPCWPSTRUCT
req.redist: 
---

# tagCWPSTRUCT structure


## -description


Defines the message parameters passed to a <b>WH_CALLWNDPROC</b> hook procedure, <a href="https://msdn.microsoft.com/en-us/library/ms644975(v=VS.85).aspx">CallWndProc</a>. 


## -struct-fields




### -field lParam

Type: <b>LPARAM</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value. 


### -field wParam

Type: <b>WPARAM</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value. 


### -field message

Type: <b>UINT</b>

The message. 


### -field hwnd

Type: <b>HWND</b>

A handle to the window to receive the message. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms644975(v=VS.85).aspx">CallWndProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>
 

 

