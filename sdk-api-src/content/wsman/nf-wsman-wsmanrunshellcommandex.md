---
UID: NF:wsman.WSManRunShellCommandEx
title: WSManRunShellCommandEx function (wsman.h)
description: Provides the same functionality as the WSManRunShellCommand function, with the addition of a command ID option.
helpviewer_keywords: ["WSManRunShellCommandEx","WSManRunShellCommandEx function [Windows Remote Management]","winrm.wsmanrunshellcommandex","wsman/WSManRunShellCommandEx"]
old-location: winrm\wsmanrunshellcommandex.htm
tech.root: winrm
ms.assetid: 3FEAB627-C38F-4709-BA17-0AFF76015A97
ms.date: 12/05/2018
ms.keywords: WSManRunShellCommandEx, WSManRunShellCommandEx function [Windows Remote Management], winrm.wsmanrunshellcommandex, wsman/WSManRunShellCommandEx
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
 - WSManRunShellCommandEx
 - wsman/WSManRunShellCommandEx
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
 - WSManRunShellCommandEx
---

# WSManRunShellCommandEx function


## -description

Provides the same functionality as the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> function, with the addition of a command ID option. If the server supports the protocol, it will create the command instance using the ID specified by the client. If a command with the specified ID already exists, the server will fail to create the command instance. This new functionality is only available when the client application passes the <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> flag as part of the call to the <a href="/windows/desktop/api/wsman/nf-wsman-wsmaninitialize">WSManInitialize</a> function.

## -parameters

### -param shell [in, out]

Specifies the shell handle returned by the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> call. This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be 0.

### -param commandId [in]

The client specified command Id.

### -param commandLine [in]

Defines a required null-terminated string that represents the command to be executed. Typically, the command is specified without any arguments, which are specified separately. However, a user can specify the command line and all of the arguments by using this parameter. If arguments are specified for the commandLine parameter, the args parameter should be <b>NULL</b>.

### -param args [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_command_arg_set">WSMAN_COMMAND_ARG_SET</a> structure that defines an array of argument values, which are passed to the command on creation. If no arguments are required, this parameter should be <b>NULL</b>.

### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a>.

### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_shell_async">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method.

### -param command [out]

Defines the command object associated with a command within a shell. This handle is returned on a successful call and is used to send and receive data and to signal the command. This handle should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.