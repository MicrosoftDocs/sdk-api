---
UID: NS:winuser.tagCBTACTIVATESTRUCT
title: CBTACTIVATESTRUCT (winuser.h)
description: Contains information passed to a WH_CBT hook procedure, CBTProc, before a window is activated.
helpviewer_keywords: ["*LPCBTACTIVATESTRUCT","CBTACTIVATESTRUCT","CBTACTIVATESTRUCT structure [Windows and Messages]","LPCBTACTIVATESTRUCT","LPCBTACTIVATESTRUCT structure pointer [Windows and Messages]","_win32_CBTACTIVATESTRUCT_str","_win32_cbtactivatestruct_str_cpp","winmsg.cbtactivatestruct","winui._win32_cbtactivatestruct_str","winuser/CBTACTIVATESTRUCT","winuser/LPCBTACTIVATESTRUCT"]
old-location: winmsg\cbtactivatestruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cbtactivatestruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPCBTACTIVATESTRUCT, CBTACTIVATESTRUCT, CBTACTIVATESTRUCT structure [Windows and Messages], LPCBTACTIVATESTRUCT, LPCBTACTIVATESTRUCT structure pointer [Windows and Messages], _win32_CBTACTIVATESTRUCT_str, _win32_cbtactivatestruct_str_cpp, winmsg.cbtactivatestruct, winui._win32_cbtactivatestruct_str, winuser/CBTACTIVATESTRUCT, winuser/LPCBTACTIVATESTRUCT'
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
targetos: Windows
req.typenames: CBTACTIVATESTRUCT, *LPCBTACTIVATESTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCBTACTIVATESTRUCT
 - winuser/tagCBTACTIVATESTRUCT
 - LPCBTACTIVATESTRUCT
 - winuser/LPCBTACTIVATESTRUCT
 - CBTACTIVATESTRUCT
 - winuser/CBTACTIVATESTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CBTACTIVATESTRUCT
---

# CBTACTIVATESTRUCT structure


## -description

Contains information passed to a <b>WH_CBT</b> hook procedure, <a href="/windows/win32/winmsg/cbtproc">CBTProc</a>, before a window is activated.

## -struct-fields

### -field fMouse

Type: <b>BOOL</b>

This member is <b>TRUE</b> if a mouse click is causing the activation or <b>FALSE</b> if it is not.

### -field hWndActive

Type: <b>HWND</b>

A handle to the active window.

## -see-also

<a href="/windows/win32/winmsg/cbtproc">CBTProc</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>