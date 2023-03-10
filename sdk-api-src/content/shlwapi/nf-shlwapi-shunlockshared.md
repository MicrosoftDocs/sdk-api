---
UID: NF:shlwapi.SHUnlockShared
title: SHUnlockShared function (shlwapi.h)
description: SHUnlockShared may be altered or unavailable.
helpviewer_keywords: ["SHUnlockShared","SHUnlockShared function [Windows Shell]","_win32_SHUnlockShared","shell.SHUnlockShared","shlwapi/SHUnlockShared"]
old-location: shell\SHUnlockShared.htm
tech.root: shell
ms.assetid: 8ecbf62b-fd0d-4a8d-bd55-42c0c3f64390
ms.date: 12/05/2018
ms.keywords: SHUnlockShared, SHUnlockShared function [Windows Shell], _win32_SHUnlockShared, shell.SHUnlockShared, shlwapi/SHUnlockShared
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHUnlockShared
 - shlwapi/SHUnlockShared
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
 - SHUnlockShared
---

# SHUnlockShared function


## -description

<p class="CCE_Message">[<b>SHUnlockShared</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Unlocks memory locked by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shlockshared">SHLockShared</a>.

## -parameters

### -param pvData [in]

Type: <b>void*</b>

A pointer to the shared memory block returned by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shlockshared">SHLockShared</a>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is <b>TRUE</b> and all modified pages within the specified range are written to the disk with low priority. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shfreeshared">SHFreeShared</a> to free the memory block.