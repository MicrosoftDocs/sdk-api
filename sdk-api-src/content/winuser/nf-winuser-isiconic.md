---
UID: NF:winuser.IsIconic
title: IsIconic function (winuser.h)
description: Determines whether the specified window is minimized (iconic).
helpviewer_keywords: ["IsIconic","IsIconic function [Windows and Messages]","_win32_IsIconic","_win32_isiconic_cpp","winmsg.isiconic","winui._win32_isiconic","winuser/IsIconic"]
old-location: winmsg\isiconic.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\isiconic.htm
ms.date: 12/05/2018
ms.keywords: IsIconic, IsIconic function [Windows and Messages], _win32_IsIconic, _win32_isiconic_cpp, winmsg.isiconic, winui._win32_isiconic, winuser/IsIconic
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsIconic
 - winuser/IsIconic
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsIconic
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# IsIconic function


## -description

Determines whether the specified window is minimized (iconic).

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the window is iconic, the return value is nonzero.

If the window is not iconic, the return value is zero.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-iszoomed">IsZoomed</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
