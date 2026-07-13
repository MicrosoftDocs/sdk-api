---
UID: NF:wtsapi32.WTSDisconnectSession
title: WTSDisconnectSession function (wtsapi32.h)
description: Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.
helpviewer_keywords: ["WTSDisconnectSession","WTSDisconnectSession function [Remote Desktop Services]","_win32_wtsdisconnectsession","termserv.wtsdisconnectsession","wtsapi32/WTSDisconnectSession"]
old-location: termserv\wtsdisconnectsession.htm
tech.root: TermServ
ms.assetid: 1e9487c2-7678-4f9c-9b0b-e6769718d027
ms.date: 12/05/2018
ms.keywords: WTSDisconnectSession, WTSDisconnectSession function [Remote Desktop Services], _win32_wtsdisconnectsession, termserv.wtsdisconnectsession, wtsapi32/WTSDisconnectSession
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSDisconnectSession
 - wtsapi32/WTSDisconnectSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSDisconnectSession
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSDisconnectSession function


## -description

Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session. If the user subsequently logs on to the same Remote Desktop Session Host (RD Session Host) server, the user is reconnected to the same session.

## -parameters

### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function, or specify <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is running.

### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify <b>WTS_CURRENT_SESSION</b>. To retrieve the identifiers of all sessions on a specified RD Session Host server, use the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> function.

To be able to disconnect another user's session, you need to have the Disconnect permission. For more information, see 
<a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

To disconnect sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.

### -param bWait [in]

Indicates whether the operation is synchronous. Specify <b>TRUE</b> to wait for the operation to complete, or <b>FALSE</b> to return immediately.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>
