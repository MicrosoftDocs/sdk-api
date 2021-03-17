---
UID: NF:shlwapi.SHFreeShared
title: SHFreeShared function (shlwapi.h)
description: SHFreeShared may be altered or unavailable.
helpviewer_keywords: ["SHFreeShared","SHFreeShared function [Windows Shell]","_win32_SHFreeShared","shell.SHFreeShared","shlwapi/SHFreeShared"]
old-location: shell\SHFreeShared.htm
tech.root: shell
ms.assetid: 5a86ae5d-8caa-4126-a22e-bc3cc7df2381
ms.date: 12/05/2018
ms.keywords: SHFreeShared, SHFreeShared function [Windows Shell], _win32_SHFreeShared, shell.SHFreeShared, shlwapi/SHFreeShared
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFreeShared
 - shlwapi/SHFreeShared
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
 - SHFreeShared
---

# SHFreeShared function


## -description

<p class="CCE_Message">[<b>SHFreeShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Frees shared memory, regardless of which process allocated it.

## -parameters

### -param hData [in]

Type: <b>HANDLE</b>

A handle to the mapped memory.

### -param dwProcessId [in]

Type: <b>DWORD</b>

The process ID of the process from which the memory was allocated.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shallocshared">SHAllocShared</a>