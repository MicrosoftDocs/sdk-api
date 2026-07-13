---
UID: NF:shlwapi.SHAllocShared
title: SHAllocShared function (shlwapi.h)
description: SHAllocShared may be altered or unavailable.
helpviewer_keywords: ["SHAllocShared","SHAllocShared function [Windows Shell]","_win32_SHAllocShared","shell.SHAllocShared","shlwapi/SHAllocShared"]
old-location: shell\SHAllocShared.htm
tech.root: shell
ms.assetid: 0388b6a0-24d9-48eb-bef2-3a1658d8bb3c
ms.date: 12/05/2018
ms.keywords: SHAllocShared, SHAllocShared function [Windows Shell], _win32_SHAllocShared, shell.SHAllocShared, shlwapi/SHAllocShared
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
req.lib: ShLwApi.Lib
req.dll: Shlwapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAllocShared
 - shlwapi/SHAllocShared
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHAllocShared
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

### -param dwProcessId [in]

Type: <b>DWORD</b>

The process ID of the process that will share memory block specified by <i>pvData</i>.

## -returns

Type: <b>HANDLE</b>

Returns a handle to the shared memory for the process specified by <i>dwDestinationProcessId</i>. Returns <b>NULL</b> if unsuccessful.

## -remarks

Use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shfreeshared">SHFreeShared</a> to free the handle when you are finished.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shfreeshared">SHFreeShared</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shlockshared">SHLockShared</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shunlockshared">SHUnlockShared</a>