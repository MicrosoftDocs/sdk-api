---
UID: NF:winbase.WTSGetActiveConsoleSessionId
title: WTSGetActiveConsoleSessionId function (winbase.h)
description: Retrieves the session identifier of the console session.
helpviewer_keywords: ["WTSGetActiveConsoleSessionId","WTSGetActiveConsoleSessionId function [Remote Desktop Services]","_win32_wtsgetactiveconsolesessionid","termserv.wtsgetactiveconsolesessionid","winbase/WTSGetActiveConsoleSessionId"]
old-location: termserv\wtsgetactiveconsolesessionid.htm
tech.root: TermServ
ms.assetid: 9aa43cfa-9518-428b-95a1-004fa23df90b
ms.date: 12/05/2018
ms.keywords: WTSGetActiveConsoleSessionId, WTSGetActiveConsoleSessionId function [Remote Desktop Services], _win32_wtsgetactiveconsolesessionid, termserv.wtsgetactiveconsolesessionid, winbase/WTSGetActiveConsoleSessionId
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSGetActiveConsoleSessionId
 - winbase/WTSGetActiveConsoleSessionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - api-ms-win-core-kernel32-legacy-l1-1-0.dll
 - kernel32legacy.dll
 - api-ms-win-core-kernel32-legacy-l1-1-1.dll
 - api-ms-win-core-kernel32-legacy-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - WTSGetActiveConsoleSessionId
---

# WTSGetActiveConsoleSessionId function


## -description

Retrieves the session identifier of the console session. The console session is the session that is currently attached to the physical console. Note that it is not necessary that Remote Desktop Services be running for this 
    function to succeed.



## -returns

The session identifier of the session that is attached to the physical console. If there is no session attached to the 
       physical console, (for example, if the physical console session is in the process of being attached or detached), this function 
       returns 0xFFFFFFFF.

## -remarks

The session identifier returned by this function is the identifier of the current physical console session. To monitor 
    the state of the current physical console session, use the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a> 
    function.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-processidtosessionid">ProcessIdToSessionId</a>



<a href="/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a>
