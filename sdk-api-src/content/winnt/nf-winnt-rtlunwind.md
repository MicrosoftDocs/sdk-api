---
UID: NF:winnt.RtlUnwind
title: RtlUnwind function (winnt.h)
description: Initiates an unwind of procedure call frames. (RtlUnwind)
helpviewer_keywords: ["RtlUnwind","RtlUnwind function","base.rtlunwind","winnt/RtlUnwind"]
old-location: base\rtlunwind.htm
tech.root: Debug
ms.assetid: 254b2547-9d3d-468f-a360-20a12e9dd82e
ms.date: 02/02/2024
ms.keywords: RtlUnwind, RtlUnwind function, base.rtlunwind, winnt/RtlUnwind
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlUnwind
 - winnt/RtlUnwind
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-rtlsupport-l1-2-2.dll
 - api-ms-win-core-rtlsupport-l1-2-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-rtlsupport-l1-1-0.dll
 - ntdll.dll
 - API-MS-Win-Core-rtlsupport-l1-2-0.dll
 - vertdll.dll
api_name:
 - RtlUnwind
---

# RtlUnwind function

## -description

Initiates an unwind of procedure call frames.

## -parameters

### -param TargetFrame [in, optional]

A pointer to the call frame that is the target of the unwind. If this parameter is `NULL`, the function performs an exit unwind.

### -param TargetIp [in, optional]

The continuation address of the unwind. This parameter is ignored if *TargetFrame* is `NULL`.

### -param ExceptionRecord [in, optional]

A pointer to an [EXCEPTION_RECORD](ns-winnt-exception_record.md) structure.

### -param ReturnValue [in]

A value to be placed in the integer function return register before continuing execution.

## -returns

This function does not return a value.

## -see-also

[EXCEPTION_RECORD](ns-winnt-exception_record.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
