---
UID: NF:wtsapi32.WTSEnumerateSessionsExA
title: WTSEnumerateSessionsExA function (wtsapi32.h)
description: Retrieves a list of sessions on a specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server. (ANSI)
helpviewer_keywords: ["WTSEnumerateSessionsExA", "wtsapi32/WTSEnumerateSessionsExA"]
old-location: termserv\wtsenumeratesessionsex.htm
tech.root: TermServ
ms.assetid: b903cf07-d3bd-4b65-9e57-88d9e1f74e0b
ms.date: 12/05/2018
ms.keywords: WTSEnumerateSessionsEx, WTSEnumerateSessionsEx function [Remote Desktop Services], WTSEnumerateSessionsExA, WTSEnumerateSessionsExW, termserv.wtsenumeratesessionsex, wtsapi32/WTSEnumerateSessionsEx, wtsapi32/WTSEnumerateSessionsExA, wtsapi32/WTSEnumerateSessionsExW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateSessionsExW (Unicode) and WTSEnumerateSessionsExA (ANSI)
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
 - WTSEnumerateSessionsExA
 - wtsapi32/WTSEnumerateSessionsExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSEnumerateSessionsEx
 - WTSEnumerateSessionsExA
 - WTSEnumerateSessionsExW
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSEnumerateSessionsExA function


## -description

Retrieves a list of sessions on a specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.

## -parameters

### -param hServer [in]

A handle to the target server. Specify a handle returned by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function. To enumerate sessions on  the RD Session Host server on which the application is running, specify <b>WTS_CURRENT_SERVER_HANDLE</b>.

### -param pLevel [in, out]

This parameter is reserved. Always set this parameter to one. On output, <b>WTSEnumerateSessionsEx</b> does not change the value of this parameter.

### -param Filter [in]

This parameter is reserved. Always set this parameter to zero.

### -param ppSessionInfo [out]

A pointer to a <b>PWTS_SESSION_INFO_1</b> variable that receives a pointer to an array of 
<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a> structures. Each structure in the array contains information about a session on the specified RD Session Host server. If you obtained a handle to an RD Virtualization Host server by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function, the array contains information about sessions on virtual machines on the server. When you have finished using the array, free it by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememoryexa">WTSFreeMemoryEx</a> function. You should also set the pointer to <b>NULL</b>.

### -param pCount [out]

A pointer to a <b>DWORD</b> variable that receives the number of 
<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a> structures returned in the <i>ppSessionInfo</i> buffer.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

To obtain information about sessions running on virtual machines on an RD Virtualization Host server, you must obtain the handle by calling the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function. To free the returned buffer, call the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememoryexa">WTSFreeMemoryEx</a> function and set the <i>WTSClassType</i> parameter to <b>WTSTypeSessionInfoLevel1</b>.

To enumerate a session, you need to have the Query Information permission for that session. For more information, see 
<a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

To enumerate sessions running on a virtual machine hosted on an RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.





> [!NOTE]
> The wtsapi32.h header defines WTSEnumerateSessionsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememoryexa">WTSFreeMemoryEx</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_info_1a">WTS_SESSION_INFO_1</a>
