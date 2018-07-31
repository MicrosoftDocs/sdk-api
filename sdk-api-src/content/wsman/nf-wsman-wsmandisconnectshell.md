---
UID: NF:wsman.WSManDisconnectShell
title: WSManDisconnectShell function
author: windows-sdk-content
description: Disconnects the network connection of an active shell and its associated commands.
old-location: winrm\wsmandisconnectshell.htm
old-project: WinRM
ms.assetid: 018F6E37-477B-4823-8597-CF80367EEB88
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSManDisconnectShell, WSManDisconnectShell function [Windows Remote Management], winrm.wsmandisconnectshell, wsman/WSManDisconnectShell
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
 - WSManDisconnectShell
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManDisconnectShell function


## -description


Disconnects the network connection of an active shell and its associated commands.


## -parameters




### -param shell [in, out]

Specifies the handle returned by a call to the 
      <a href="https://msdn.microsoft.com/901c0a2d-d25f-451c-8d6c-83662f1f1061">WSManCreateShell</a> function. This parameter cannot 
      be <b>NULL</b>.


### -param flags

Can be a <b>WSMAN_FLAG_SERVER_BUFFERING_MODE_DROP</b> flag or a 
      <b>WSMAN_FLAG_SERVER_BUFFERING_MODE_BLOCK</b> flag.


### -param disconnectInfo [in]

A pointer to a 
      <a href="https://msdn.microsoft.com/CFC855E8-25C9-45A1-8D59-55AD5D4A75F3">WSMAN_SHELL_DISCONNECT_INFO</a> structure 
      that specifies an idle time-out that the server session may enforce. If this parameter is 
      <b>NULL</b>, the server session idle time-out will not be changed.


### -param async [in]

Defines an asynchronous structure to contain an optional user context and a mandatory callback function. 
      For more information, see <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a>. This 
      parameter cannot be <b>NULL</b>.


## -returns



This function does not return a value.




## -remarks



This function suspends network connection to an actively connected server session. Any operations performed on 
    the shell instance, like <a href="https://msdn.microsoft.com/8f5c89f8-418c-4a4d-9a52-0fc01ec636b2">WSManRunShellCommand</a>, 
    <a href="https://msdn.microsoft.com/2336671e-0f60-407f-86a2-9918bbf7f66b">WSManSendShellInput</a>, or 
    <a href="https://msdn.microsoft.com/9954097d-3e27-4f56-bf8c-3d9aba5c19b5">WSManSignalShell</a>, are bound to complete before 
    disconnection. This ensures that any data sent through 
    <b>WSManSendShellInput</b> is received by the server 
    session before the shell disconnects. The client can optionally modify the server buffering mode by using flags. 
    The following behavior is observed:

<ul>
<li>
<b>WSMAN_FLAG_SERVER_BUFFERING_MODE_DROP</b>–When buffers are full, 
       the server drops earlier data in response stream buffers to ensure the corresponding command operation 
       continues to run.

</li>
<li>
<b>WSMAN_FLAG_SERVER_BUFFERING_MODE_BLOCK</b>–When response stream 
       buffers are full, the server blocks command execution. If no flag is specified, the server continues to use 
       either the configured mode or the mode specified when the shell was created. In case of a network failure, if 
       the client is unable to contact the session to disconnect the shell, the following error is returned:

<b>ERROR_WINRS_SHELL_DISCONNECT_OPERATION_NOT_GRACEFUL</b>

The client session still goes into a disconnected state, but it is not guaranteed that any prior operations 
       have completed before the session is disconnected.

</li>
</ul>


