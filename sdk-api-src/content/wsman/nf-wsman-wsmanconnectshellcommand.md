---
UID: NF:wsman.WSManConnectShellCommand
title: WSManConnectShellCommand function (wsman.h)
description: Connects to an existing command running in a shell.
helpviewer_keywords: ["WSManConnectShellCommand","WSManConnectShellCommand function [Windows Remote Management]","winrm.wsmanconnectshellcommand","wsman/WSManConnectShellCommand"]
old-location: winrm\wsmanconnectshellcommand.htm
tech.root: winrm
ms.assetid: 860EC6F8-35A9-4C12-9247-4E14E6B1D66A
ms.date: 12/05/2018
ms.keywords: WSManConnectShellCommand, WSManConnectShellCommand function [Windows Remote Management], winrm.wsmanconnectshellcommand, wsman/WSManConnectShellCommand
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
 - WSManConnectShellCommand
 - wsman/WSManConnectShellCommand
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
 - WSManConnectShellCommand
---

# WSManConnectShellCommand function


## -description

Connects to an existing  command running in a shell.

## -parameters

### -param shell [in, out]

Specifies the shell handle returned by the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call. This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be zero.

### -param commandID [in]

A null-terminated string that identifies a specific command, currently running in the server session, that the client intends to connect to.

### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a>.

### -param connectXml [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that defines an open context for the connect shell operation. The content must be a valid XML string. This parameter can be <b>NULL</b>.

### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.

### -param command [out]

This handle is returned on a successful call and is used to send and receive data and to signal the command. When you have finished using this handle, close it by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.