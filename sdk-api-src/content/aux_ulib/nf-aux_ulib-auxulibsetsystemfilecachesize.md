---
UID: NF:aux_ulib.AuxUlibSetSystemFileCacheSize
title: AuxUlibSetSystemFileCacheSize function (aux_ulib.h)
description: Sets the current file system cache size.
helpviewer_keywords: ["AuxUlibSetSystemFileCacheSize","AuxUlibSetSystemFileCacheSize function [Windows API]","aux_ulib/AuxUlibSetSystemFileCacheSize","winprog.auxulibsetsystemfilecachesize_func"]
old-location: winprog\auxulibsetsystemfilecachesize_func.htm
tech.root: winprog
ms.assetid: 2a6ee33e-91dc-4f6d-bdb7-a93b7478b58e
ms.date: 12/05/2018
ms.keywords: AuxUlibSetSystemFileCacheSize, AuxUlibSetSystemFileCacheSize function [Windows API], aux_ulib/AuxUlibSetSystemFileCacheSize, winprog.auxulibsetsystemfilecachesize_func
req.header: aux_ulib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Aux_ulib.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Auxiliary API library version 1.0 or later
ms.custom: 19H1
f1_keywords:
 - AuxUlibSetSystemFileCacheSize
 - aux_ulib/AuxUlibSetSystemFileCacheSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Aux_ulib.lib
api_name:
 - AuxUlibSetSystemFileCacheSize
---

# AuxUlibSetSystemFileCacheSize function


## -description

Sets the current file system cache size.

As of Windows Server 2003 with Service Pack 1 (SP1), this function has been superseded by the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-setsystemfilecachesize">SetSystemFileCacheSize</a> function.

## -parameters

### -param MinimumFileCacheSize [in]

The minimum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.

### -param MaximumFileCacheSize [in]

The maximum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.

### -param Flags [in]

This parameter is reserved for future use and must be zero.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You must call the <a href="/windows/desktop/api/aux_ulib/nf-aux_ulib-auxulibinitialize">AuxUlibInitialize</a> function before calling this function.

The caller must have enabled the SE_INCREASE_QUOTA_NAME privilege in the active token.

## -see-also

<a href="/windows/desktop/api/aux_ulib/nf-aux_ulib-auxulibinitialize">AuxUlibInitialize</a>