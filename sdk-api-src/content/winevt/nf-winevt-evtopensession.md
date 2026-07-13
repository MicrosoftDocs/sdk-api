---
UID: NF:winevt.EvtOpenSession
title: EvtOpenSession function (winevt.h)
description: Establishes a connection to a remote computer that you can use when calling the other Windows Event Log functions.
helpviewer_keywords: ["EvtOpenSession","EvtOpenSession function [EventLog]","wes.evtopensession","winevt/EvtOpenSession"]
old-location: wes\evtopensession.htm
tech.root: wes
ms.assetid: 26f1745c-dcca-4452-872e-1fffe20f049c
ms.date: 12/05/2018
ms.keywords: EvtOpenSession, EvtOpenSession function [EventLog], wes.evtopensession, winevt/EvtOpenSession
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtOpenSession
 - winevt/EvtOpenSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtOpenSession
---

# EvtOpenSession function


## -description

Establishes a connection to a remote computer that you can use when calling the other Windows Event Log functions.

## -parameters

### -param LoginClass [in]

The connection method to use to connect to the remote computer. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_login_class">EVT_LOGIN_CLASS</a> enumeration.

### -param Login [in]

A <a href="/windows/desktop/api/winevt/ns-winevt-evt_rpc_login">EVT_RPC_LOGIN</a> structure that identifies the remote computer that you want to connect to, the user's credentials, and the type of authentication to use when connecting.

### -param Timeout [in]

Reserved. Must be zero.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a session handle that you can use to access event log information on the remote computer; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

When you are finished with the session handle, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function. Closing the session handle will also close all open handles created in the session (closing the open handles cancels any current activity on those handles).

To connect to the remote computer, the remote computer must enable the "Remote Event Log Management" Windows Firewall exception; otherwise, when you try to use the session handle, the call will error with RPC_S_SERVER_UNAVAILABLE. The computer to which you are connecting must be running Windows Vista or later.

This function does not validate the credentials; the credentials are validated the first time you try to use the session handle. If the credentials are not valid, the call will fail with ERROR_ACCESS_DENIED.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/accessing-remote-computers">Accessing Remote Computers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/ne-winevt-evt_login_class">EVT_LOGIN_CLASS</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a>