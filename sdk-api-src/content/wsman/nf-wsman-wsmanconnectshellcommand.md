---
UID: NF:wsman.WSManConnectShellCommand
title: WSManConnectShellCommand function
author: windows-sdk-content
description: Connects to an existing command running in a shell.
old-location: winrm\wsmanconnectshellcommand.htm
old-project: WinRM
ms.assetid: 860EC6F8-35A9-4C12-9247-4E14E6B1D66A
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: WSManConnectShellCommand, WSManConnectShellCommand function [Windows Remote Management], winrm.wsmanconnectshellcommand, wsman/WSManConnectShellCommand
ms.prod: windows
ms.technology: windows-sdk
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
 - WSManConnectShellCommand
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManConnectShellCommand function


## -description


Connects to an existing  command running in a shell.


## -parameters




### -param shell [in, out]

Specifies the shell handle returned by the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call. This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be zero.


### -param commandID [in]

A null-terminated string that identifies a specific command, currently running in the server session, that the client intends to connect to.


### -param options [in, optional]

Defines a set of options for the command. These options are passed to the service to modify or refine the command execution. This parameter can be <b>NULL</b>. For more information about the options, see <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a>.


### -param connectXml [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that defines an open context for the connect shell operation. The content must be a valid XML string. This parameter can be <b>NULL</b>.


### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.


### -param command [out]

This handle is returned on a successful call and is used to send and receive data and to signal the command. When you have finished using this handle, close it by calling the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> method. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



