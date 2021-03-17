---
UID: NF:wsman.WSManDisconnectShell
title: WSManDisconnectShell function (wsman.h)
description: Disconnects the network connection of an active shell and its associated commands.
helpviewer_keywords: ["WSManDisconnectShell","WSManDisconnectShell function [Windows Remote Management]","winrm.wsmandisconnectshell","wsman/WSManDisconnectShell"]
old-location: winrm\wsmandisconnectshell.htm
tech.root: winrm
ms.assetid: 018F6E37-477B-4823-8597-CF80367EEB88
ms.date: 12/05/2018
ms.keywords: WSManDisconnectShell, WSManDisconnectShell function [Windows Remote Management], winrm.wsmandisconnectshell, wsman/WSManDisconnectShell
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSManDisconnectShell
 - wsman/WSManDisconnectShell
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManDisconnectShell
---

# WSManDisconnectShell function


## -description

Disconnects the network connection of an active shell and its associated commands.

## -parameters

### -param shell [in, out]

Specifies the handle returned by a call to the 
      <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> function. This parameter cannot 
      be <b>NULL</b>.

### -param flags

Can be a <b>WSMAN_FLAG_SERVER_BUFFERING_MODE_DROP</b> flag or a 
      <b>WSMAN_FLAG_SERVER_BUFFERING_MODE_BLOCK</b> flag.

### -param disconnectInfo [in]

A pointer to a 
      <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_disconnect_info">WSMAN_SHELL_DISCONNECT_INFO</a> structure 
      that specifies an idle time-out that the server session may enforce. If this parameter is 
      <b>NULL</b>, the server session idle time-out will not be changed.

### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. 
      For more information, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a>. This 
      parameter cannot be <b>NULL</b>.

## -remarks

This function suspends network connection to an actively connected server session. Any operations performed on 
    the shell instance, like <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a>, 
    <a href="/windows/desktop/api/wsman/nf-wsman-wsmansendshellinput">WSManSendShellInput</a>, or 
    <a href="/windows/desktop/api/wsman/nf-wsman-wsmansignalshell">WSManSignalShell</a>, are bound to complete before 
    disconnection. This ensures that any data sent through 
    <b>WSManSendShellInput</b> is received by the server 
    session before the shell disconnects. The client can optionally modify the server buffering mode by using flags. 
    The following behavior is observed:

<ul>
<li>
<b>WSMAN_FLAG_SERVER_BUFFERING_MODE_DROP</b>–When buffers are full, 
       the server drops earlier data in response stream buffers to ensure the corresponding command operation 
       continues to run.

</li>
<li>
<b>WSMAN_FLAG_SERVER_BUFFERING_MODE_BLOCK</b>–When response stream 
       buffers are full, the server blocks command execution. If no flag is specified, the server continues to use 
       either the configured mode or the mode specified when the shell was created. In case of a network failure, if 
       the client is unable to contact the session to disconnect the shell, the following error is returned:

<b>ERROR_WINRS_SHELL_DISCONNECT_OPERATION_NOT_GRACEFUL</b>

The client session still goes into a disconnected state, but it is not guaranteed that any prior operations 
       have completed before the session is disconnected.

</li>
</ul>