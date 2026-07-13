---
UID: NF:winuser.IsGUIThread
title: IsGUIThread function (winuser.h)
description: Determines whether the calling thread is already a GUI thread. It can also optionally convert the thread to a GUI thread.
helpviewer_keywords: ["IsGUIThread","IsGUIThread function [Windows and Messages]","_win32_IsGUIThread","_win32_isguithread_cpp","winmsg.isguithread","winui._win32_isguithread","winuser/IsGUIThread"]
old-location: winmsg\isguithread.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\isguithread.htm
ms.date: 12/05/2018
ms.keywords: IsGUIThread, IsGUIThread function [Windows and Messages], _win32_IsGUIThread, _win32_isguithread_cpp, winmsg.isguithread, winui._win32_isguithread, winuser/IsGUIThread
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsGUIThread
 - winuser/IsGUIThread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - ext-ms-win-ntuser-window-l1-1-4.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - ext-ms-win-ntuser-window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - IsGUIThread
---

# IsGUIThread function


## -description

Determines whether the calling thread is already a GUI thread. It can also optionally convert the thread to a GUI thread.

## -parameters

### -param bConvert [in]

Type: <b>BOOL</b>

If <b>TRUE</b> and the thread is not a GUI thread, convert the thread to a GUI thread.

## -returns

Type: <b>BOOL</b>

The function returns a nonzero value in the following situations: 

<ul>
<li>If the calling thread is already a GUI thread.</li>
<li>If <i>bConvert</i> is <b>TRUE</b> and the function successfully converts the thread to a GUI thread.</li>
</ul>
Otherwise, the function returns zero.

If <i>bConvert</i> is <b>TRUE</b> and the function cannot successfully convert the thread to a GUI thread,  <b>IsGUIThread</b> returns <b>ERROR_NOT_ENOUGH_MEMORY</b>.

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>