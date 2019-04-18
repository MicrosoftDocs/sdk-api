---
UID: NC:ntsecpkg.LSA_CREATE_THREAD
title: LSA_CREATE_THREAD (ntsecpkg.h)
author: windows-sdk-content
description: A wrapper for the Windows CreateThread function that should be used by the Local Security Authority (LSA).
old-location: security\createthread.htm
tech.root: SecAuthN
ms.assetid: dc02abb9-ab05-4a7f-a125-15530619633b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateThread, CreateThread callback function [Security], LSA_CREATE_THREAD, LSA_CREATE_THREAD callback, _ssp_createthread, ntsecpkg/CreateThread, security.createthread
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Ntsecpkg.h
api_name:
 - CreateThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_CREATE_THREAD callback function


## -description


The <b>CreateThread</b> function is a wrapper for the Windows 
<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a> function that should be used by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA). It creates a thread that the LSA can track, attaches debugging information to threads it starts, and provides special exception handling to protect the LSA process.


## -parameters




### -param SecurityAttributes [in]

Pointer to a <b>SEC_ATTRS</b> structure that determines whether the returned handle can be inherited by child processes.


### -param StackSize [in]

Specifies the initial commit size of the stack, in bytes.


### -param StartFunction [in]

Pointer to the application-defined function of type <b>SEC_THREAD_START</b> to be executed by the thread.


### -param ThreadParameter [in]

Pointer to a single parameter value passed to the thread.


### -param CreationFlags [in]

Specifies flags that control the creation of the thread.


### -param ThreadId [out]

Pointer to a variable that receives the thread identifier.


## -returns



If the function succeeds, the return value is a handle to the new thread. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A pointer to the <b>CreateThread</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.

For more information, see the Windows 
<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a> function.




## -see-also




<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

