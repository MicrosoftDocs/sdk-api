---
UID: NF:wtsapi32.WTSQueryUserToken
title: WTSQueryUserToken function (wtsapi32.h)
description: Obtains the primary access token of the logged-on user specified by the session ID.
helpviewer_keywords: ["WTSQueryUserToken","WTSQueryUserToken function [Remote Desktop Services]","_win32_wtsqueryusertoken","termserv.wtsqueryusertoken","wtsapi32/WTSQueryUserToken"]
old-location: termserv\wtsqueryusertoken.htm
tech.root: TermServ
ms.assetid: 5b33b67a-ab19-4c09-94a2-1ab8008551a8
ms.date: 12/05/2018
ms.keywords: WTSQueryUserToken, WTSQueryUserToken function [Remote Desktop Services], _win32_wtsqueryusertoken, termserv.wtsqueryusertoken, wtsapi32/WTSQueryUserToken
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
 - WTSQueryUserToken
 - wtsapi32/WTSQueryUserToken
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
 - WTSQueryUserToken
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSQueryUserToken function


## -description

Obtains the primary access token of the logged-on user specified by the session ID. To call 
    this function successfully, the calling application must be running within the context of the 
    <a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a> and have the 
    <b>SE_TCB_NAME</b> privilege.
<div class="alert"><b>Caution</b>  <b>WTSQueryUserToken</b> is 
    intended for highly trusted services. Service providers must use caution that they do not leak user tokens when 
    calling this function. Service providers must close token handles after they have finished using them.</div><div> </div>

## -parameters

### -param SessionId [in]

A Remote Desktop Services session identifier. Any program running in the context of a service will have a 
       session identifier of zero (0). You can use the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> function to retrieve 
      the identifiers of all sessions on a specified RD Session Host server.

To be able to query information for another user's session, you need to have the Query Information 
       permission. For more information, see 
       <a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services 
       Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration 
       administrative tool.

### -param phToken [out]

If the function succeeds, receives a pointer to the token handle for the logged-on user. Note that you must 
      call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close this 
      handle.

## -returns

If the function succeeds, the return value is a nonzero value, and the <i>phToken</i> 
       parameter points to the primary token of the user.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For information about primary tokens, see 
    <a href="/windows/desktop/SecAuthZ/access-tokens">Access Tokens</a>. For more information about 
    account privileges, see 
    <a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a> 
    and <a href="/windows/desktop/SecAuthZ/authorization-constants">Authorization Constants</a>.

See <a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a> for 
    information about the privileges associated with that account.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a>
