---
UID: NF:winnt.RtlCaptureContext
title: RtlCaptureContext function (winnt.h)
description: Retrieves a context record in the context of the caller.
helpviewer_keywords: ["RtlCaptureContext","RtlCaptureContext function","base.rtlcapturecontext","winnt/RtlCaptureContext"]
old-location: base\rtlcapturecontext.htm
tech.root: Debug
ms.assetid: e2ce0cde-43ab-4681-be66-bd7509fd6ca2
ms.date: 02/02/2024
ms.keywords: RtlCaptureContext, RtlCaptureContext function, base.rtlcapturecontext, winnt/RtlCaptureContext
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlCaptureContext
 - winnt/RtlCaptureContext
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
 - RtlCaptureContext
---

# RtlCaptureContext function

## -description

Retrieves a context record in the context of the caller.

## -parameters

### -param ContextRecord [out]

A pointer to a [CONTEXT](ns-winnt-arm64_nt_context.md) structure.

## -returns

This function does not return a value.

## -see-also

[CONTEXT](ns-winnt-arm64_nt_context.md)

[RtlRestoreContext](nf-winnt-rtlrestorecontext.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
