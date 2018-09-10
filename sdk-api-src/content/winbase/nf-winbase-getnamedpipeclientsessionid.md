---
UID: NF:winbase.GetNamedPipeClientSessionId
title: GetNamedPipeClientSessionId function
author: windows-sdk-content
description: Retrieves the client session identifier for the specified named pipe.
old-location: base\getnamedpipeclientsessionid.htm
tech.root: ipc
ms.assetid: b3ea0b7f-fead-4369-b87a-2f522a2a1984
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetNamedPipeClientSessionId, GetNamedPipeClientSessionId function, base.getnamedpipeclientsessionid, winbase/GetNamedPipeClientSessionId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetNamedPipeClientSessionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNamedPipeClientSessionId function


## -description


Retrieves the client session identifier for the specified named pipe.


## -parameters




### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> function.


### -param ClientSessionId [out]

The session identifier.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.




## -see-also




<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a>



<a href="https://msdn.microsoft.com/cd628d6d-aa13-4762-893b-42f6cf7a2ba6">GetNamedPipeServerSessionId</a>



<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>
 

 

