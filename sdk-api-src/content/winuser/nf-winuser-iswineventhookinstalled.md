---
UID: NF:winuser.IsWinEventHookInstalled
title: IsWinEventHookInstalled function (winuser.h)
description: Determines whether there is an installed WinEvent hook that might be notified of a specified event.
helpviewer_keywords: ["IsWinEventHookInstalled","IsWinEventHookInstalled function [Windows Accessibility]","_msaa_IsWinEventHookInstalled","msaa.iswineventhookinstalled","winauto.iswineventhookinstalled","winuser/IsWinEventHookInstalled"]
old-location: winauto\iswineventhookinstalled.htm
tech.root: WinAuto
ms.assetid: bc1e97ad-748d-420a-8c9a-72a555b685e1
ms.date: 12/05/2018
ms.keywords: IsWinEventHookInstalled, IsWinEventHookInstalled function [Windows Accessibility], _msaa_IsWinEventHookInstalled, msaa.iswineventhookinstalled, winauto.iswineventhookinstalled, winuser/IsWinEventHookInstalled
req.header: winuser.h
req.include-header: 
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
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IsWinEventHookInstalled
 - winuser/IsWinEventHookInstalled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Winevent-l1-1-0.dll
 - minuser.dll
api_name:
 - IsWinEventHookInstalled
req.apiset: ext-ms-win-ntuser-server-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# IsWinEventHookInstalled function


## -description

Determines whether there is an installed WinEvent hook that might be notified of a specified event.

## -parameters

### -param event [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The event constant that hooks might be notified of. The function checks whether there is an installed hook for this event constant.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If there is a hook to be notified of the specified event, the return value is <b>TRUE</b>.

If there are no hooks to be notified of the specified event, the return value is <b>FALSE</b>.

## -remarks

This method is guaranteed to never return a false negative. If this method returns <b>FALSE</b>, it means that no hooks in the system would be notified of the event. However, this method may return a false positive. In other words, it may return <b>TRUE</b> even though there are no hooks that would be notified. Thus, it is safe for components to circumvent some work if this method returns <b>FALSE</b>. 

Event hooks can be installed at any time, so server developers should not cache the return value for long periods of time.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-setwineventhook">SetWinEventHook</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unhookwinevent">UnhookWinEvent</a>
