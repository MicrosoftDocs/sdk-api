---
UID: NF:winnt.RtlVirtualUnwind
title: RtlVirtualUnwind function (winnt.h)
description: Retrieves the invocation context of the function that precedes the specified function context.
helpviewer_keywords: ["RtlVirtualUnwind","RtlVirtualUnwind function","UNW_FLAG_CHAININFO","UNW_FLAG_EHANDLER","UNW_FLAG_NHANDLER","UNW_FLAG_UHANDLER","base.rtlvirtualunwind","winnt/RtlVirtualUnwind"]
old-location: base\rtlvirtualunwind.htm
tech.root: Debug
ms.assetid: 78d60f7a-0e16-4856-8aca-c251ab066b83
ms.date: 02/02/2024
ms.keywords: RtlVirtualUnwind, RtlVirtualUnwind function, UNW_FLAG_CHAININFO, UNW_FLAG_EHANDLER, UNW_FLAG_NHANDLER, UNW_FLAG_UHANDLER, base.rtlvirtualunwind, winnt/RtlVirtualUnwind
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
ms.custom: 19H1
f1_keywords:
 - RtlVirtualUnwind
 - winnt/RtlVirtualUnwind
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
 - RtlVirtualUnwind
---

# RtlVirtualUnwind function

## -description

Retrieves the invocation context of the function that precedes the specified function context.

> [!NOTE]
> This function is not implemented on all processor platforms and the implementation is different on each platform that supports it. The following prototype lists all the potential parameters and their application. Read further for processor-specific function prototypes.

## -parameters

### -param HandlerType [in]

The handler type. This parameter can be one of the following values.

This parameter is only present on x64.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UNW_FLAG_NHANDLER"></a><a id="unw_flag_nhandler"></a><dl>
<dt><b>UNW_FLAG_NHANDLER</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The function has no handler.

</td>
</tr>
<tr>
<td width="40%"><a id="UNW_FLAG_EHANDLER"></a><a id="unw_flag_ehandler"></a><dl>
<dt><b>UNW_FLAG_EHANDLER</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The function has an exception handler that should be called.

</td>
</tr>
<tr>
<td width="40%"><a id="UNW_FLAG_UHANDLER"></a><a id="unw_flag_uhandler"></a><dl>
<dt><b>UNW_FLAG_UHANDLER</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The function has a termination handler that should be called when unwinding an exception.

</td>
</tr>
<tr>
<td width="40%"><a id="UNW_FLAG_CHAININFO"></a><a id="unw_flag_chaininfo"></a><dl>
<dt><b>UNW_FLAG_CHAININFO</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The <b>FunctionEntry</b> member is the contents of a previous function table entry.

</td>
</tr>
</table>

### -param ImageBase [in]

The base address of the module to which the function belongs.

### -param ControlPc [in]

The virtual address where control left the specified function.

### -param FunctionEntry [in]

The address of the function table entry for the specified function. To obtain the function table entry, call the [RtlLookupFunctionEntry](nf-winnt-rtllookupfunctionentry.md) function.

### -param ContextRecord [in, out]

A pointer to a [CONTEXT](ns-winnt-arm64_nt_context.md) structure that represents the context of the previous frame.

### -param HandlerData [out]

The location of the PC. If this parameter is 0, the PC is in the prologue, epilogue, or a null frame region of the function. If this parameter is 1, the PC is in the body of the function.

This parameter is not present on x64.

### -param EstablisherFrame [out]

A pointer to a **FRAME_POINTERS** structure that receives the establisher frame pointer value. The real frame pointer is defined only if *InFunction* is `1`.

This parameter is of type **PULONG64** on x64.

### -param ContextPointers [in, out, optional]

An optional pointer to a context pointers structure.

## -returns

This function returns a pointer to an **EXCEPTION_ROUTINE** callback function.

## -remarks

The complete list of epilogue markers for x64 is as follows:

- ret
- ret *n*
- rep ret
- jmp *imm8* | *imm32* where the target is outside the function being unwound
- jmp qword ptr *imm32*
- rex.w jmp *reg*

## -see-also

[CONTEXT](ns-winnt-arm64_nt_context.md)

[EXCEPTION_RECORD](ns-winnt-exception_record.md)

[RtlLookupFunctionEntry](nf-winnt-rtllookupfunctionentry.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
