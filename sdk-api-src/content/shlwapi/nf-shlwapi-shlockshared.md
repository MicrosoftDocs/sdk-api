---
UID: NF:shlwapi.SHLockShared
title: SHLockShared function
author: windows-sdk-content
description: SHLockShared may be altered or unavailable.
old-location: shell\SHLockShared.htm
tech.root: shell
ms.assetid: 5b948044-6cec-4649-a266-21959154f999
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: SHLockShared, SHLockShared function [Windows Shell], _win32_SHLockShared, shell.SHLockShared, shlwapi/SHLockShared
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHLockShared
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHLockShared function


## -description


<p class="CCE_Message">[<b>SHLockShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Maps a block of memory from a specified process into the calling process.


## -parameters




### -param hData [in]

Type: <b>HANDLE</b>

A handle to the memory you want to map into the calling process.


### -param dwProcessId [in]

Type: <b>DWORD</b>

The process ID of the process from which you want to map the block of memory.


## -returns



Returns a void pointer to the shared memory. Returns <b>NULL</b> if unsuccessful.




## -remarks



Call <a href="https://msdn.microsoft.com/8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390">SHUnlockShared</a> to unlock the memory that this function maps. Call <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to release the memory.



