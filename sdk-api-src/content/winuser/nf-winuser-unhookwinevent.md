---
UID: NF:winuser.UnhookWinEvent
title: UnhookWinEvent function (winuser.h)
description: Removes an event hook function created by a previous call to SetWinEventHook.
helpviewer_keywords: ["UnhookWinEvent","UnhookWinEvent function [Windows Accessibility]","_msaa_UnhookWinEvent","msaa.unhookwinevent","winauto.unhookwinevent","winuser/UnhookWinEvent"]
old-location: winauto\unhookwinevent.htm
tech.root: WinAuto
ms.assetid: 5cffb279-85e1-4f7a-8bbb-d0d618f6afcd
ms.date: 12/05/2018
ms.keywords: UnhookWinEvent, UnhookWinEvent function [Windows Accessibility], _msaa_UnhookWinEvent, msaa.unhookwinevent, winauto.unhookwinevent, winuser/UnhookWinEvent
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - UnhookWinEvent
 - winuser/UnhookWinEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-winevent-ext-l1-1-0.dll
 - ext-ms-win-ntuser-server-l1-1-1.dll
 - ext-ms-win-ntuser-server-l1-1-0.dll
 - user32.dll
 - API-MS-Win-RTCore-NTUser-Winevent-l1-1-0.dll
 - minuser.dll
api_name:
 - UnhookWinEvent
---

# UnhookWinEvent function


## -description

Removes an event hook function created by a previous call to <a href="/windows/desktop/api/winuser/nf-winuser-setwineventhook">SetWinEventHook</a>.

## -parameters

### -param hWinEventHook [in]

Type: <b>HWINEVENTHOOK</b>

Handle to the event hook returned in the previous call to <a href="/windows/desktop/api/winuser/nf-winuser-setwineventhook">SetWinEventHook</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If successful, returns <b>TRUE</b>; otherwise, returns <b>FALSE</b>.

Three common errors cause this function to fail:

<ul>
<li>The <i>hWinEventHook</i> parameter is <b>NULL</b> or not valid.</li>
<li>The event hook specified by <i>hWinEventHook</i> was already removed.</li>
<li><b>UnhookWinEvent</b> is called from a thread that is different from the original call to <a href="/windows/desktop/api/winuser/nf-winuser-setwineventhook">SetWinEventHook</a>.</li>
</ul>

## -remarks

This function removes the event hook specified by <i>hWinEventHook</i> that prevents the corresponding callback function from receiving further event notifications. If the client's thread ends, the system automatically calls this function.

Call this function from the same thread that installed the event hook. <b>UnhookWinEvent</b> fails if called from a thread different from the call that corresponds to <a href="/windows/desktop/api/winuser/nf-winuser-setwineventhook">SetWinEventHook</a>.

If WINEVENT_INCONTEXT was specified when this event hook was installed, the system attempts to unload the corresponding DLL from all processes that loaded it. Although unloading does not occur immediately, the hook function is not called after <b>UnhookWinEvent</b> returns. For more information on WINEVENT_INCONTEXT, see <a href="/windows/desktop/WinAuto/in-context-hook-functions">In-Context Hook Functions</a>.