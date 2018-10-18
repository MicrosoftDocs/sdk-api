---
UID: NF:shlwapi.SHUnlockShared
title: SHUnlockShared function
author: windows-sdk-content
description: SHUnlockShared may be altered or unavailable.
old-location: shell\SHUnlockShared.htm
tech.root: shell
ms.assetid: 8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: SHUnlockShared, SHUnlockShared function [Windows Shell], _win32_SHUnlockShared, shell.SHUnlockShared, shlwapi/SHUnlockShared
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
req.lib: Shlwapi.lib
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
 - SHUnlockShared
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHUnlockShared function


## -description


<p class="CCE_Message">[<b>SHUnlockShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Unlocks memory locked by <a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>.


## -parameters




### -param pvData [in]

Type: <b>void*</b>

A pointer to the shared memory block returned by <a href="https://msdn.microsoft.com/5b948044-6cec-4649-a266-21959154f999">SHLockShared</a>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is <b>TRUE</b> and all modified pages within the specified range are written to the disk with low priority. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Call <a href="https://msdn.microsoft.com/5a86ae5d-8caa-4126-a22e-bc3cc7df2381">SHFreeShared</a> to free the memory block.



