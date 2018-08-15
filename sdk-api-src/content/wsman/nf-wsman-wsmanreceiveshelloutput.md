---
UID: NF:wsman.WSManReceiveShellOutput
title: WSManReceiveShellOutput function
author: windows-sdk-content
description: Retrieves output from a running command or from the shell.
old-location: winrm\wsmanreceiveshelloutput.htm
old-project: winrm
ms.assetid: cc64f212-9897-4a58-b3f1-bc2093f593ba
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSManReceiveShellOutput, WSManReceiveShellOutput function [Windows Remote Management], winrm.wsmanreceiveshelloutput, wsman/WSManReceiveShellOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wsman.h
req.include-header: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
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
 - WSManReceiveShellOutput
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManReceiveShellOutput function


## -description


Retrieves output from a running command or from the shell.


## -parameters




### -param shell [in, out]

Specifies the shell handle returned by a <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> call.  This parameter cannot be <b>NULL</b>.


### -param command [in, optional]

Specifies the command handle returned by a <a href="https://msdn.microsoft.com/8f5c89f8-418c-4a4d-9a52-0fc01ec636b2">WSManRunShellCommand</a> call.


### -param flags

Reserved for future use. Must be set to zero.


### -param desiredStreamSet [in, optional]

Specifies the requested output from a particular stream or a list of streams.


### -param async [in]

Defines an asynchronous structure. The asynchronous structure contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be <b>NULL</b> and should be closed by calling the <a href="https://msdn.microsoft.com/4fd51026-6a48-42ef-a245-7593a615c103">WSManCloseOperation</a> method.


### -param receiveOperation [out]

Defines the operation handle for the receive operation. This handle is returned from a successful call of the function and can be used to asynchronously cancel the receive operation. This handle should be closed by calling the <a href="https://msdn.microsoft.com/4fd51026-6a48-42ef-a245-7593a615c103">WSManCloseOperation</a> method. This parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.



