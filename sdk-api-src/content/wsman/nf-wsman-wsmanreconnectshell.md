---
UID: NF:wsman.WSManReconnectShell
title: WSManReconnectShell function (wsman.h)
author: windows-sdk-content
description: Reconnects a previously disconnected shell session. To reconnect the shell session's associated commands, use WSManReconnectShellCommand.
old-location: winrm\wsmanreconnectshell.htm
tech.root: winrm
ms.assetid: 92D9D3FE-73A1-45FA-AD8A-344AB909C6F7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSManReconnectShell, WSManReconnectShell function [Windows Remote Management], winrm.wsmanreconnectshell, wsman/WSManReconnectShell
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManReconnectShell
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSManReconnectShell function


## -description


Reconnects a previously disconnected shell session. To reconnect the shell session's associated commands, use <a href="https://msdn.microsoft.com/3894BB74-4EAA-46D3-ACB2-AFDD3517A9C1">WSManReconnectShellCommand</a>.


## -parameters




### -param shell [in, out]

Specifies the handle returned by a call to the <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> function. This parameter cannot be <b>NULL</b>.


### -param flags

This parameter is reserved for future use and must be set to zero.


### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. For more information, see  <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a>. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



