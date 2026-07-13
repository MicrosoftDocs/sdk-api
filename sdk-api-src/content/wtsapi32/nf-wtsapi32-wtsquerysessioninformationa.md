---
UID: NF:wtsapi32.WTSQuerySessionInformationA
title: WTSQuerySessionInformationA function (wtsapi32.h)
description: Retrieves session information for the specified session on the specified Remote Desktop Session Host (RD Session Host) server. (ANSI)
helpviewer_keywords: ["WTSQuerySessionInformationA", "wtsapi32/WTSQuerySessionInformationA"]
old-location: termserv\wtsquerysessioninformation.htm
tech.root: TermServ
ms.assetid: d52345a4-0408-4ea9-ba71-349910143752
ms.date: 12/05/2018
ms.keywords: WTSQuerySessionInformation, WTSQuerySessionInformation function [Remote Desktop Services], WTSQuerySessionInformationA, WTSQuerySessionInformationW, _win32_wtsquerysessioninformation, termserv.wtsquerysessioninformation, wtsapi32/WTSQuerySessionInformation, wtsapi32/WTSQuerySessionInformationA, wtsapi32/WTSQuerySessionInformationW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSQuerySessionInformationW (Unicode) and WTSQuerySessionInformationA (ANSI)
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
 - WTSQuerySessionInformationA
 - wtsapi32/WTSQuerySessionInformationA
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
 - WTSQuerySessionInformation
 - WTSQuerySessionInformationA
 - WTSQuerySessionInformationW
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSQuerySessionInformationA function


## -description

Retrieves session information for the specified session on the specified Remote Desktop Session Host (RD Session Host) server. It can be used 
    to query session information on local and remote RD Session Host servers.

## -parameters

### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application 
      is running.

### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the session in which the calling application is running 
      (or the current session) specify <b>WTS_CURRENT_SESSION</b>. Only specify 
      <b>WTS_CURRENT_SESSION</b> when obtaining session information on the local server. If 
      <b>WTS_CURRENT_SESSION</b> is specified when querying session information on a remote server, 
      the returned session information will be inconsistent. Do not use the returned data.

You can use the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> 
       function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To query information for another user's session, you must have Query Information permission. For more 
       information, see <a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services 
       Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative 
       tool.

### -param WTSInfoClass [in]

A value of the <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_info_class">WTS_INFO_CLASS</a> enumeration that indicates the type of 
    session information to retrieve in a call to the 
    <b>WTSQuerySessionInformation</b> function.

### -param ppBuffer [out]

A pointer to a variable that receives a pointer to the requested information. The format and contents of the 
      data depend on the information class specified in the <i>WTSInfoClass</i> parameter. To free 
      the returned buffer, call the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> 
      function.

### -param pBytesReturned [out]

A pointer to a variable that receives the size, in bytes, of the data returned in 
      <i>ppBuffer</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To retrieve the session ID for the current session when Remote Desktop Services is running, call 
    <b>WTSQuerySessionInformation</b> and specify 
    <b>WTS_CURRENT_SESSION</b> for the <i>SessionId</i> parameter and 
    <b>WTSSessionId</b> for the <i>WTSInfoClass</i> parameter. The session ID 
    will be returned in the <i>ppBuffer</i> parameter. If Remote Desktop Services is not running, calls 
    to <b>WTSQuerySessionInformation</b> fail. In 
    this situation, you can retrieve the current session ID by calling the 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-processidtosessionid">ProcessIdToSessionId</a> function.

To determine whether your application is running on the physical console, you must specify 
    <b>WTS_CURRENT_SESSION</b> for the <i>SessionId</i> parameter, and 
    <b>WTSClientProtocolType</b> as the <i>WTSInfoClass</i> parameter. 
    If <i>ppBuffer</i> is "0", the session is attached to the physical console.





> [!NOTE]
> The wtsapi32.h header defines WTSQuerySessionInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsconfiginfoa">WTSCONFIGINFO</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoexa">WTSINFOEX</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_address">WTS_CLIENT_ADDRESS</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_info_class">WTS_INFO_CLASS</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_session_address">WTS_SESSION_ADDRESS</a>
