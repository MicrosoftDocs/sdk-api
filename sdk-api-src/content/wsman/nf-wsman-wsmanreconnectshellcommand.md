---
UID: NF:wsman.WSManReconnectShellCommand
title: WSManReconnectShellCommand function (wsman.h)
description: Reconnects a previously disconnected command.
helpviewer_keywords: ["WSManReconnectShellCommand","WSManReconnectShellCommand function [Windows Remote Management]","winrm.wsmanreconnectshellcommand","wsman/WSManReconnectShellCommand"]
old-location: winrm\wsmanreconnectshellcommand.htm
tech.root: winrm
ms.assetid: 3894BB74-4EAA-46D3-ACB2-AFDD3517A9C1
ms.date: 12/05/2018
ms.keywords: WSManReconnectShellCommand, WSManReconnectShellCommand function [Windows Remote Management], winrm.wsmanreconnectshellcommand, wsman/WSManReconnectShellCommand
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
 - WSManReconnectShellCommand
 - wsman/WSManReconnectShellCommand
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
 - WSManReconnectShellCommand
---

# WSManReconnectShellCommand function


## -description

Reconnects a previously disconnected command.

## -parameters

### -param commandHandle [in, out]

Specifies the handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> call or a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanconnectshellcommand">WSManConnectShellCommand</a> call. This parameter cannot be NULL.

### -param flags

Reserved for future use. Must be set to zero.

### -param async [in]

Defines an asynchronous structure which will contain an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be NULL.