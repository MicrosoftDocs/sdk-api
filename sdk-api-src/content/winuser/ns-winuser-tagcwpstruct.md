---
UID: NS:winuser.tagCWPSTRUCT
title: tagCWPSTRUCT
author: windows-sdk-content
description: Defines the message parameters passed to a WH_CALLWNDPROC hook procedure, CallWndProc.
old-location: winmsg\cwpstruct.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cwpstruct.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPCWPSTRUCT, *NPCWPSTRUCT, *PCWPSTRUCT, CWPSTRUCT, CWPSTRUCT structure [Windows and Messages], LPCWPSTRUCT, LPCWPSTRUCT structure pointer [Windows and Messages], PCWPSTRUCT, PCWPSTRUCT structure pointer [Windows and Messages], _win32_CWPSTRUCT_str, _win32_cwpstruct_str_cpp, tagCWPSTRUCT, winmsg.cwpstruct, winui._win32_cwpstruct_str, winuser/CWPSTRUCT, winuser/LPCWPSTRUCT, winuser/PCWPSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CWPSTRUCT, *PCWPSTRUCT, *NPCWPSTRUCT, *LPCWPSTRUCT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagCWPSTRUCT structure


## -description


Defines the message parameters passed to a <b>WH_CALLWNDPROC</b> hook procedure, <a href="https://msdn.microsoft.com/25df5ac2-f007-4683-ba89-537dc7a3c15e">CallWndProc</a>. 


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




<a href="https://msdn.microsoft.com/25df5ac2-f007-4683-ba89-537dc7a3c15e">CallWndProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a>
 

 

