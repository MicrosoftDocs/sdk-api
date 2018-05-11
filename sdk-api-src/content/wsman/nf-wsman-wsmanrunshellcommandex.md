---
UID: NF:wsman.WSManRunShellCommandEx
title: WSManRunShellCommandEx function
author: windows-driver-content
description: Provides the same functionality as the WSManRunShellCommand function, with the addition of a command ID option.
old-location: winrm\wsmanrunshellcommandex.htm
old-project: WinRM
ms.assetid: 3FEAB627-C38F-4709-BA17-0AFF76015A97
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: WSManRunShellCommandEx, WSManRunShellCommandEx function [Windows Remote Management], winrm.wsmanrunshellcommandex, wsman/WSManRunShellCommandEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WSManSessionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsmSvc.dll
api_name:
-	WSManRunShellCommandEx
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManRunShellCommandEx function


## -description


Provides the same functionality as the <a href="https://msdn.microsoft.com/8f5c89f8-418c-4a4d-9a52-0fc01ec636b2">WSManRunShellCommand</a> function, with the addition of a command ID option. If the server supports the protocol, it will create the command instance using the ID specified by the client. If a command with the specified ID already exists, the server will fail to create the command instance. This new functionality is only available when the client application passes the <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> flag as part of the call to the <a href="https://msdn.microsoft.com/5aa1f451-0d12-4079-9477-1971fc084df2">WSManInitialize</a> function.


## -parameters




### -param shell [in, out]

Specifies the shell handle returned by the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call. This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be 0.


### -param commandId

TBD


### -param commandLine [in]

Defines a required null-terminated string that represents the command to be executed. Typically, the command is specified without any arguments, which are specified separately. However, a user can specify the command line and all of the arguments by using this parameter. If arguments are specified for the commandLine parameter, the args parameter should be <b>NULL</b>.


### -param args [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/0904851f-e275-445c-b3fa-e5974d037322">WSMAN_COMMAND_ARG_SET</a> structure that defines an array of argument values, which are passed to the command on creation. If no arguments are required, this parameter should be <b>NULL</b>.


### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a>.


### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method.


### -param command [out]

Defines the command object associated with a command within a shell. This handle is returned on a successful call and is used to send and receive data and to signal the command. This handle should be closed by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.


#### - commandID [in]

The client specified command Id.


## -returns



This function does not return a value.



