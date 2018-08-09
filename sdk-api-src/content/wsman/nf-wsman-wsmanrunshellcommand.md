---
UID: NF:wsman.WSManRunShellCommand
title: WSManRunShellCommand function
author: windows-sdk-content
description: Starts the execution of a command within an existing shell and does not wait for the completion of the command.
old-location: winrm\wsmanrunshellcommand.htm
old-project: winrm
ms.assetid: 8f5c89f8-418c-4a4d-9a52-0fc01ec636b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSManRunShellCommand, WSManRunShellCommand function [Windows Remote Management], winrm.wsmanrunshellcommand, wsman/WSManRunShellCommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSManSessionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManRunShellCommand
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManRunShellCommand function


## -description


Starts the execution of a command within an existing shell and does not wait for the completion of the command.


## -parameters




### -param shell [in, out]

Specifies the shell handle returned by the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be zero.


### -param commandLine [in]

Defines a required <b>null</b>-terminated string that represents the command to be executed. Typically, the command is specified without any arguments, which are specified separately. However, a user can specify the command line and all of the arguments by using this parameter. If arguments are specified for the <i>commandLine</i> parameter, the <i>args</i> parameter should be <b>NULL</b>.


### -param args [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/0904851f-e275-445c-b3fa-e5974d037322">WSMAN_COMMAND_ARG_SET</a> structure that defines an array of argument values, which are passed to the command on creation. If no arguments are required, this parameter should be <b>NULL</b>.


### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a>.


### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information.  This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method.


### -param command [out]

Defines the command object associated with a command within a shell. This handle is returned on a successful call and is used to send and receive data and to signal the command. This handle should be closed  by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



