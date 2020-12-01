---
UID: NF:wsman.WSManReconnectShell
title: WSManReconnectShell function (wsman.h)
description: Reconnects a previously disconnected shell session. To reconnect the shell session's associated commands, use WSManReconnectShellCommand.
helpviewer_keywords: ["WSManReconnectShell","WSManReconnectShell function [Windows Remote Management]","winrm.wsmanreconnectshell","wsman/WSManReconnectShell"]
old-location: winrm\wsmanreconnectshell.htm
tech.root: winrm
ms.assetid: 92D9D3FE-73A1-45FA-AD8A-344AB909C6F7
ms.date: 12/05/2018
ms.keywords: WSManReconnectShell, WSManReconnectShell function [Windows Remote Management], winrm.wsmanreconnectshell, wsman/WSManReconnectShell
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
 - WSManReconnectShell
 - wsman/WSManReconnectShell
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
 - WSManReconnectShell
---

# WSManReconnectShell function


## -description

Reconnects a previously disconnected shell session. To reconnect the shell session's associated commands, use <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreconnectshellcommand">WSManReconnectShellCommand</a>.

## -parameters

### -param shell [in, out]

Specifies the handle returned by a call to the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> function. This parameter cannot be <b>NULL</b>.

### -param flags

This parameter is reserved for future use and must be set to zero.

### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see  <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.