---
UID: NF:winnt.RtlLookupFunctionEntry
title: RtlLookupFunctionEntry function (winnt.h)
description: Searches the active function tables for an entry that corresponds to the specified PC value.
helpviewer_keywords: ["RtlLookupFunctionEntry","RtlLookupFunctionEntry function","base.rtllookupfunctionentry","winnt/RtlLookupFunctionEntry"]
old-location: base\rtllookupfunctionentry.htm
tech.root: Debug
ms.assetid: 624b97fb-0453-4f47-b6bd-92aa14705e78
ms.date: 02/02/2024
ms.keywords: RtlLookupFunctionEntry, RtlLookupFunctionEntry function, base.rtllookupfunctionentry, winnt/RtlLookupFunctionEntry
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
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
ms.custom: 19H1
f1_keywords:
 - RtlLookupFunctionEntry
 - winnt/RtlLookupFunctionEntry
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
 - RtlLookupFunctionEntry
---

# RtlLookupFunctionEntry function

## -description

Searches the active function tables for an entry that corresponds to the specified PC value.

## -parameters

### -param ControlPc [in]

The virtual address of an instruction bundle within the function.

### -param ImageBase [out]

The base address of module to which the function belongs.

### -param HistoryTable [out]

The global pointer value of the module.

This parameter has a different declaration on x64 and ARM systems. For more information, see x64 Definition and ARM Definition.

## -returns

If there is no entry in the function table for the specified PC, the function returns `NULL`. Otherwise, the function returns the address of the function table entry that corresponds to the specified PC.

## -see-also

[RtlUnwindEx](nf-winnt-rtlunwindex.md)

[RtlVirtualUnwind](nf-winnt-rtlvirtualunwind.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
