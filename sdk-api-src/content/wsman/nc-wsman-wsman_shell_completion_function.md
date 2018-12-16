---
UID: NC:wsman.WSMAN_SHELL_COMPLETION_FUNCTION
title: WSMAN_SHELL_COMPLETION_FUNCTION
author: windows-sdk-content
description: The callback function that is called for shell operations, which result in a remote request.
old-location: winrm\wsman_shell_completion_function.htm
tech.root: winrm
ms.assetid: 705732a8-7584-42cf-be9b-dd36b35bba37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_SHELL_COMPLETION_FUNCTION, WSMAN_SHELL_COMPLETION_FUNCTION callback, WSMAN_SHELL_COMPLETION_FUNCTION callback function [Windows Remote Management], winrm.wsman_shell_completion_function, wsman/WSMAN_SHELL_COMPLETION_FUNCTION
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_COMPLETION_FUNCTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, and     Windows Vista with SP2
---

# WSMAN_SHELL_COMPLETION_FUNCTION callback function


## -description


The callback function that is called for shell operations, which result in a remote request.


## -parameters




### -param operationContext [in, optional]

Represents user-defined context passed to the WinRM (WinRM) Client Shell 
      application programming interface (API) .


### -param flags

Specifies one or more flags from the 
      <a href="https://msdn.microsoft.com/ce4c664d-bc69-415a-955d-7761f58a25e2">WSManCallbackFlags</a> enumeration.


### -param *error [in]

Defines the <a href="https://msdn.microsoft.com/6705b560-9c72-4cb9-a290-f7c65cd470b2">WSMAN_ERROR</a> structure, which is 
      valid in the callback only.


### -param shell [in]

Specifies the shell handle  associated with the user context.  The shell handle  must be closed by calling 
      the <a href="https://msdn.microsoft.com/1da452ef-5842-4d8d-941b-09fa57393ebb">WSManCloseShell</a> method.


### -param command [in, optional]

Specifies the command handle associated with the user context. The command handle must be closed by calling 
      the <a href="https://msdn.microsoft.com/41ef2a6d-af1a-4a51-b01d-262380f01187">WSManCloseCommand</a> API method.


### -param operationHandle [in, optional]

Defines the operation handle associated with the user context. The operation handle is valid only for 
      callbacks that are associated with 
      <a href="https://msdn.microsoft.com/cc64f212-9897-4a58-b3f1-bc2093f593ba">WSManReceiveShellOutput</a>, 
      <a href="https://msdn.microsoft.com/2336671e-0f60-407f-86a2-9918bbf7f66b">WSManSendShellInput</a>, and 
      <a href="https://msdn.microsoft.com/9954097d-3e27-4f56-bf8c-3d9aba5c19b5">WSManSignalShell</a> calls. This handle must be closed 
      by calling the <a href="https://msdn.microsoft.com/4fd51026-6a48-42ef-a245-7593a615c103">WSManCloseOperation</a> 
      method.


### -param *data [in, optional]

Defines the output data from the command or shell as a result of a 
      <a href="https://msdn.microsoft.com/cc64f212-9897-4a58-b3f1-bc2093f593ba">WSManReceiveShellOutput</a> call. For more 
      information about the output data, see the 
      <a href="https://msdn.microsoft.com/e649a4f0-37ae-40cb-9245-e1b792034c8a">WSMAN_RECEIVE_DATA_RESULT</a> structure.


## -returns



This callback function does not return a value.



