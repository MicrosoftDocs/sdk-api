---
UID: NF:wsman.WSManRunShellCommand
title: WSManRunShellCommand function (wsman.h)
description: Starts the execution of a command within an existing shell and does not wait for the completion of the command.
helpviewer_keywords: ["WSManRunShellCommand","WSManRunShellCommand function [Windows Remote Management]","winrm.wsmanrunshellcommand","wsman/WSManRunShellCommand"]
old-location: winrm\wsmanrunshellcommand.htm
tech.root: winrm
ms.assetid: 8f5c89f8-418c-4a4d-9a52-0fc01ec636b2
ms.date: 12/05/2018
ms.keywords: WSManRunShellCommand, WSManRunShellCommand function [Windows Remote Management], winrm.wsmanrunshellcommand, wsman/WSManRunShellCommand
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManRunShellCommand
 - wsman/WSManRunShellCommand
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
 - WSManRunShellCommand
---

# WSManRunShellCommand function


## -description

Starts the execution of a command within an existing shell and does not wait for the completion of the command.

## -parameters

### -param shell [in, out]

Specifies the shell handle returned by the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be zero.

### -param commandLine [in]

Defines a required <b>null</b>-terminated string that represents the command to be executed. Typically, the command is specified without any arguments, which are specified separately. However, a user can specify the command line and all of the arguments by using this parameter. If arguments are specified for the <i>commandLine</i> parameter, the <i>args</i> parameter should be <b>NULL</b>.

### -param args [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_command_arg_set">WSMAN_COMMAND_ARG_SET</a> structure that defines an array of argument values, which are passed to the command on creation. If no arguments are required, this parameter should be <b>NULL</b>.

### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a>.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method.

### -param command [out]

Defines the command object associated with a command within a shell. This handle is returned on a successful call and is used to send and receive data and to signal the command. This handle should be closed  by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.