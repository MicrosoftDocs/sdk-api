---
UID: NF:winnt.RtlIsEcCode
tech.root: Kernel
title: RtlIsEcCode
ms.date: 02/23/2023
targetos: Windows
description: Returns a value indicating if the code pointed to by the supplied pointer is ARM emulation-compatible (ARM64EC).
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: api-ms-win-core-rtlsupport-l1-2-2.dll
req.header: winnt.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllEcport
api_location:
 - api-ms-win-core-rtlsupport-l1-2-1.dll
 - api-ms-win-core-rtlsupport-l1-2-0.dll
 - api-ms-win-core-rtlsupport-l1-1-0.dll
 - api-ms-win-core-rtlsupport-l1-2-2.dll
api_name:
 - RtlIsEcCode
f1_keywords:
 - RtlIsEcCode
 - winnt/RtlIsEcCode
dev_langs:
 - c++
helpviewer_keywords:
 - RtlIsEcCode
---

## -description

Returns a value indicating if the code pointed to by the supplied pointer is ARM emulation-compatible (ARM64EC).

## -parameters

### -param CodePointer

A ULONG64 representing a pointer to the code being to be queried.

## -returns

**TRUE** if the code is ARM emulation compatible; otherwise, **FALSE**.

## -remarks

## -see-also

