---
UID: NS:winuser.tagMOUSEHOOKSTRUCT
title: tagMOUSEHOOKSTRUCT
author: windows-sdk-content
description: Contains information about a mouse event passed to a WH_MOUSE hook procedure, MouseProc.
old-location: winmsg\mousehookstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\mousehookstruct.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPMOUSEHOOKSTRUCT, *PMOUSEHOOKSTRUCT, LPMOUSEHOOKSTRUCT, LPMOUSEHOOKSTRUCT structure pointer [Windows and Messages], MOUSEHOOKSTRUCT, MOUSEHOOKSTRUCT structure [Windows and Messages], PMOUSEHOOKSTRUCT, PMOUSEHOOKSTRUCT structure pointer [Windows and Messages], _win32_MOUSEHOOKSTRUCT_str, _win32_mousehookstruct_str_cpp, tagMOUSEHOOKSTRUCT, winmsg.mousehookstruct, winui._win32_mousehookstruct_str, winuser/LPMOUSEHOOKSTRUCT, winuser/MOUSEHOOKSTRUCT, winuser/PMOUSEHOOKSTRUCT"
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
 - MOUSEHOOKSTRUCT
product: Windows
targetos: Windows
req.typenames: MOUSEHOOKSTRUCT, *LPMOUSEHOOKSTRUCT, *PMOUSEHOOKSTRUCT
req.redist: 
---

# tagMOUSEHOOKSTRUCT structure


## -description


Contains information about a mouse event passed to a <b>WH_MOUSE</b> hook procedure, <a href="https://msdn.microsoft.com/en-us/library/ms644988(v=VS.85).aspx">MouseProc</a>. 


## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The x- and y-coordinates of the cursor, in screen coordinates. 


### -field hwnd

Type: <b>HWND</b>

A handle to the window that will receive the mouse message corresponding to the mouse event. 


### -field wHitTestCode

Type: <b>UINT</b>

The hit-test value. For a list of hit-test values, see the description of the <a href="https://msdn.microsoft.com/en-us/library/ms645618(v=VS.85).aspx">WM_NCHITTEST</a> message. 


### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with the message. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644988(v=VS.85).aspx">MouseProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645618(v=VS.85).aspx">WM_NCHITTEST</a>
 

 

