---
UID: NF:wtsapi32.WTSEnumerateSessionsW
title: WTSEnumerateSessionsW function (wtsapi32.h)
description: Retrieves a list of sessions on a Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["WTSEnumerateSessions", "WTSEnumerateSessions function [Remote Desktop Services]", "WTSEnumerateSessionsW", "_win32_wtsenumeratesessions", "termserv.wtsenumeratesessions", "wtsapi32/WTSEnumerateSessions", "wtsapi32/WTSEnumerateSessionsW"]
old-location: termserv\wtsenumeratesessions.htm
tech.root: TermServ
ms.assetid: 6f9dd7d4-48dc-411c-85f1-cd1239d1e106
ms.date: 12/05/2018
ms.keywords: WTSEnumerateSessions, WTSEnumerateSessions function [Remote Desktop Services], WTSEnumerateSessionsA, WTSEnumerateSessionsW, _win32_wtsenumeratesessions, termserv.wtsenumeratesessions, wtsapi32/WTSEnumerateSessions, wtsapi32/WTSEnumerateSessionsA, wtsapi32/WTSEnumerateSessionsW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateSessionsW (Unicode) and WTSEnumerateSessionsA (ANSI)
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
 - WTSEnumerateSessionsW
 - wtsapi32/WTSEnumerateSessionsW
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
 - WTSEnumerateSessions
 - WTSEnumerateSessionsA
 - WTSEnumerateSessionsW
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSEnumerateSessionsW function


## -description

Retrieves a list of sessions on a Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param hServer [in]

A handle to the RD Session Host server.

<div class="alert"><b>Note</b>  You can use the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> functions to retrieve a handle to a specific server, or  <b>WTS_CURRENT_SERVER_HANDLE</b> to use the RD Session Host server that hosts your application.</div>
<div> </div>

### -param Reserved [in]

This parameter is reserved. It must be zero.

### -param Version [in]

The version of the enumeration request. This parameter must be 1.

### -param ppSessionInfo [out]

A pointer to an array of <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_infoa">WTS_SESSION_INFO</a> structures that represent the retrieved sessions. To free the returned buffer, call the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function.

<b>Session permissions:  </b><ul>
<li>To enumerate a session, you must enable the query information permission. For more information, see 
<a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>.</li>
<li>To change permissions on a session, use the Remote Desktop Services Configuration administrative tool.</li>
<li>To enumerate sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.</li>
</ul>

### -param pCount [out]

A pointer to the number of 
<b>WTS_SESSION_INFO</b> structures returned in the <i>ppSessionInfo</i> parameter.

## -returns

Returns zero if this function fails. If this function succeeds, a nonzero value is returned.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks



> [!NOTE]
> The wtsapi32.h header defines WTSEnumerateSessions as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_infoa">WTS_SESSION_INFO</a>
