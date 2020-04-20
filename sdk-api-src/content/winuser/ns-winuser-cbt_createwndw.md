---
UID: NS:winuser.tagCBT_CREATEWNDW
title: CBT_CREATEWNDW (winuser.h)
description: Contains information passed to a WH_CBT hook procedure, CBTProc, before a window is created.helpviewer_keywords: ["*LPCBT_CREATEWNDW","CBT_CREATEWND","CBT_CREATEWND structure [Windows and Messages]","CBT_CREATEWNDA","CBT_CREATEWNDW","LPCBT_CREATEWND","LPCBT_CREATEWND structure pointer [Windows and Messages]","_win32_CBT_CREATEWND_str","_win32_cbt_createwnd_str_cpp","winmsg.cbt_createwnd","winui._win32_cbt_createwnd_str","winuser/CBT_CREATEWND","winuser/CBT_CREATEWNDA","winuser/CBT_CREATEWNDW","winuser/LPCBT_CREATEWND"]
old-location: winmsg\cbt_createwnd.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cbt_createwnd.htm
ms.date: 12/05/2018
ms.keywords: '*LPCBT_CREATEWNDW, CBT_CREATEWND, CBT_CREATEWND structure [Windows and Messages], CBT_CREATEWNDA, CBT_CREATEWNDW, LPCBT_CREATEWND, LPCBT_CREATEWND structure pointer [Windows and Messages], _win32_CBT_CREATEWND_str, _win32_cbt_createwnd_str_cpp, winmsg.cbt_createwnd, winui._win32_cbt_createwnd_str, winuser/CBT_CREATEWND, winuser/CBT_CREATEWNDA, winuser/CBT_CREATEWNDW, winuser/LPCBT_CREATEWND'
f1_keywords:
- winuser/CBT_CREATEWND
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
req.unicode-ansi: CBT_CREATEWNDW (Unicode) and CBT_CREATEWNDA (ANSI)
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
- CBT_CREATEWND
- CBT_CREATEWNDA
- CBT_CREATEWNDW
targetos: Windows
req.typenames: CBT_CREATEWNDW, *LPCBT_CREATEWNDW
req.redist: 
ms.custom: 19H1
---

# CBT_CREATEWNDW structure


## -description


Contains information passed to a <b>WH_CBT</b> hook procedure, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)">CBTProc</a>, before a window is created. 


## -struct-fields




### -field lpcs

Type: <b>LPCREATESTRUCT</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a> structure that contains initialization parameters for the window about to be created. 


### -field hwndInsertAfter

Type: <b>HWND</b>

A handle to the window whose position in the Z order precedes that of the window being created. This member can also be <b>NULL</b>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)">CBTProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/hooks">Hooks</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>
 

 

