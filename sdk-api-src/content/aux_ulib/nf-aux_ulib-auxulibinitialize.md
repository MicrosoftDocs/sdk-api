---
UID: NF:aux_ulib.AuxUlibInitialize
title: AuxUlibInitialize function (aux_ulib.h)
description: Initializes the Aux_ulib library.
helpviewer_keywords: ["AuxUlibInitialize","AuxUlibInitialize function [Windows API]","aux_ulib/AuxUlibInitialize","winprog.auxulibinitialize_func"]
old-location: winprog\auxulibinitialize_func.htm
tech.root: winprog
ms.assetid: 2e46e323-669c-4fcd-b3e0-d1e4ec700c64
ms.date: 12/05/2018
ms.keywords: AuxUlibInitialize, AuxUlibInitialize function [Windows API], aux_ulib/AuxUlibInitialize, winprog.auxulibinitialize_func
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
 - AuxUlibInitialize
 - aux_ulib/AuxUlibInitialize
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
 - AuxUlibInitialize
---

# AuxUlibInitialize function


## -description

Initializes the Aux_ulib library. This function must be called before any
    other function in the library can be called.



## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/aux_ulib/nf-aux_ulib-auxulibsetsystemfilecachesize">AuxUlibSetSystemFileCacheSize</a>
