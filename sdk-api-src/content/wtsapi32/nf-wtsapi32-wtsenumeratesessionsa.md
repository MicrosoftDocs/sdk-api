---
UID: NF:wtsapi32.WTSEnumerateSessionsA
title: WTSEnumerateSessionsA function (wtsapi32.h)
author: windows-sdk-content
description: Retrieves a list of sessions on a Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsenumeratesessions.htm
tech.root: TermServ
ms.assetid: 6f9dd7d4-48dc-411c-85f1-cd1239d1e106
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSEnumerateSessions, WTSEnumerateSessions function [Remote Desktop Services], WTSEnumerateSessionsA, WTSEnumerateSessionsW, _win32_wtsenumeratesessions, termserv.wtsenumeratesessions, wtsapi32/WTSEnumerateSessions, wtsapi32/WTSEnumerateSessionsA, wtsapi32/WTSEnumerateSessionsW
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSEnumerateSessions
 - WTSEnumerateSessionsA
 - WTSEnumerateSessionsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSEnumerateSessionsA function


## -description


Retrieves a list of sessions on a Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

A handle to the RD Session Host server.

<div class="alert"><b>Note</b>  You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> functions to retrieve a handle to a specific server, or  <b>WTS_CURRENT_SERVER_HANDLE</b> to use the RD Session Host server that hosts your application.</div>
<div> </div>

### -param Reserved [in]

This parameter is reserved. It must be zero.


### -param Version [in]

The version of the enumeration request. This parameter must be 1.


### -param ppSessionInfo [out]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-_wts_session_infoa">WTS_SESSION_INFO</a> structures that represent the retrieved sessions. To free the returned buffer, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function.

<b>Session permissions:  </b><ul>
<li>To enumerate a session, you must enable the query information permission. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>.</li>
<li>To change permissions on a session, use the Remote Desktop Services Configuration administrative tool.</li>
<li>To enumerate sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.</li>
</ul>



### -param pCount [out]

A pointer to the number of 
<b>WTS_SESSION_INFO</b> structures returned in the <i>ppSessionInfo</i> parameter.


## -returns



Returns zero if this function fails. If this function succeeds, a nonzero value is returned.

To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



For more information, and an extended example on how to use this function, see the following <a href="https://support.microsoft.com/en-us/kb/291789">kb article</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-_wts_session_infoa">WTS_SESSION_INFO</a>
 

 

