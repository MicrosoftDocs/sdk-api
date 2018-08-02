---
UID: NS:wsman._WSMAN_SHELL_ASYNC
title: "_WSMAN_SHELL_ASYNC"
author: windows-sdk-content
description: Defines an asynchronous structure to be passed to all shell operations.
old-location: winrm\wsman_shell_async.htm
old-project: WinRM
ms.assetid: 9391e1a8-7048-49b8-9dc4-1da25b190238
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSMAN_SHELL_ASYNC, WSMAN_SHELL_ASYNC structure [Windows Remote Management], _WSMAN_SHELL_ASYNC, winrm.wsman_shell_async, wsman/WSMAN_SHELL_ASYNC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WSMAN_SHELL_ASYNC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_ASYNC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_SHELL_ASYNC structure


## -description


Defines an asynchronous structure to be passed to all shell operations. It contains an optional user context and the callback function.


## -struct-fields




### -field operationContext

Specifies the optional user context associated with the operation.


### -field completionFunction

Specifies the <a href="https://msdn.microsoft.com/705732a8-7584-42cf-be9b-dd36b35bba37">WSMAN_SHELL_COMPLETION_FUNCTION</a> callback function for the operation.

