---
UID: NF:shlobj_core.SHAlloc
title: SHAlloc function (shlobj_core.h)
description: Allocates memory from the Shell's heap.
helpviewer_keywords: ["SHAlloc","SHAlloc function [Windows Shell]","_win32_SHAlloc","shell.SHAlloc","shlobj_core/SHAlloc"]
old-location: shell\SHAlloc.htm
tech.root: shell
ms.assetid: 621e4335-1484-4111-9cfe-7ae5c6d5c609
ms.date: 12/05/2018
ms.keywords: SHAlloc, SHAlloc function [Windows Shell], _win32_SHAlloc, shell.SHAlloc, shlobj_core/SHAlloc
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAlloc
 - shlobj_core/SHAlloc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHAlloc
---

# SHAlloc function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> instead.]

Allocates memory from the Shell's heap.

## -parameters

### -param cb [in]

Type: <b>SIZE_T</b>

The number of bytes of memory to allocate.

## -returns

Type: <b>LPVOID</b>

A pointer to the allocated memory.

## -remarks

You can free this memory by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfree">SHFree</a>.