---
UID: NF:wtsapi32.WTSLogoffSession
title: WTSLogoffSession function (wtsapi32.h)
description: Logs off a specified Remote Desktop Services session.
helpviewer_keywords: ["WTSLogoffSession","WTSLogoffSession function [Remote Desktop Services]","_win32_wtslogoffsession","termserv.wtslogoffsession","wtsapi32/WTSLogoffSession"]
old-location: termserv\wtslogoffsession.htm
tech.root: TermServ
ms.assetid: dba7b6fb-f906-40d1-baae-6ee7b8cfe86d
ms.date: 12/05/2018
ms.keywords: WTSLogoffSession, WTSLogoffSession function [Remote Desktop Services], _win32_wtslogoffsession, termserv.wtslogoffsession, wtsapi32/WTSLogoffSession
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
 - WTSLogoffSession
 - wtsapi32/WTSLogoffSession
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
 - WTSLogoffSession
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSLogoffSession function


## -description

Logs off a specified Remote Desktop Services session.

## -parameters

### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function, or specify <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is running.

### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify <b>WTS_CURRENT_SESSION</b>. You can use the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To be able to log off another user's session, you need to have the Reset permission. For more information, see 
<a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

To log off sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.

### -param bWait [in]

Indicates whether the operation is synchronous.

If <i>bWait</i> is <b>TRUE</b>, the function returns when the session is logged off.

If <i>bWait</i> is <b>FALSE</b>, the function returns immediately. To verify that the session has been logged off, specify the session identifier in a call to the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function. 
<b>WTSQuerySessionInformation</b> returns zero if the session is logged off.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>
