---
UID: NF:winnt.RtlPcToFileHeader
title: RtlPcToFileHeader function (winnt.h)
description: Retrieves the base address of the image that contains the specified PC value.
helpviewer_keywords: ["RtlPcToFileHeader","RtlPcToFileHeader function","base.rtlpctofileheader","winnt/RtlPcToFileHeader"]
old-location: base\rtlpctofileheader.htm
tech.root: Debug
ms.assetid: 690c9f20-d471-49c9-a40c-28926f03acac
ms.date: 02/02/2024
ms.keywords: RtlPcToFileHeader, RtlPcToFileHeader function, base.rtlpctofileheader, winnt/RtlPcToFileHeader
req.header: winnt.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
ms.custom: 19H1
f1_keywords:
 - RtlPcToFileHeader
 - winnt/RtlPcToFileHeader
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
 - RtlPcToFileHeader
---

# RtlPcToFileHeader function

## -description

Retrieves the base address of the image that contains the specified PC value.

## -parameters

### -param PcValue [in]

The PC value. The function searches all modules mapped into the address space of the calling process for a module that contains this value.

### -param BaseOfImage [out]

The base address of the image containing the PC value. This value must be added to any relative addresses in the headers to locate the image.

## -returns

If the PC value is found, the function returns the base address of the image that contains the PC value.

If no image contains the PC value, the function returns `NULL`.

## -see-also

[RtlLookupFunctionEntry](nf-winnt-rtllookupfunctionentry.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
