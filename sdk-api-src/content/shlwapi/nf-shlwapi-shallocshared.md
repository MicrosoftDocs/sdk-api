---
UID: NF:shlwapi.SHAllocShared
title: SHAllocShared function
author: windows-sdk-content
description: SHAllocShared may be altered or unavailable.
old-location: shell\SHAllocShared.htm
old-project: shell
ms.assetid: 0388b6a0-24d9-48eb-bef2-3a1658d8bb3c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHAllocShared, SHAllocShared function [Windows Shell], _win32_SHAllocShared, shell.SHAllocShared, shlwapi/SHAllocShared
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHAllocShared
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SHAllocShared function


## -description


<p class="CCE_Message">[<b>SHAllocShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Allocates a handle in a specified process to a copy of a specified memory block in the calling process.


## -parameters




### -param pvData [in, optional]

Type: <b>const void*</b>

A pointer to the memory block in the calling process that is to be copied. You can set this parameter to <b>NULL</b> if you want to share a block of memory without copying any data to it.


### -param dwSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the memory block pointed to by <i>pvData</i>.


### -param dwProcessId

TBD




#### - dwDestinationProcessId [in]

Type: <b>DWORD</b>

The process ID of the process that will share memory block specified by <i>pvData</i>.


## -returns



Type: <b>HANDLE</b>

Returns a handle to the shared memory for the process specified by <i>dwDestinationProcessId</i>. Returns <b>NULL</b> if unsuccessful.




## -remarks



Use <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to free the handle when you are finished.




## -see-also




<a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a>



<a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>



<a href="https://msdn.microsoft.com/8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390">SHUnlockShared</a>
 

 

