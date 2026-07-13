---
UID: NF:winnt.RtlDeleteGrowableFunctionTable
title: RtlDeleteGrowableFunctionTable function (winnt.h)
description: Informs the system that a previously reported dynamic function table is no longer in use.
helpviewer_keywords: ["RtlDeleteGrowableFunctionTable","RtlDeleteGrowableFunctionTable function","base.rtldeletegrowablefunctiontable","winnt/RtlDeleteGrowableFunctionTable"]
old-location: base\rtldeletegrowablefunctiontable.htm
tech.root: Debug
ms.assetid: 2ae4eef2-5cdc-4ebf-9285-ef6a1a4e9197
ms.date: 12/05/2018
ms.keywords: RtlDeleteGrowableFunctionTable, RtlDeleteGrowableFunctionTable function, base.rtldeletegrowablefunctiontable, winnt/RtlDeleteGrowableFunctionTable
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdll.lib
req.dll: Ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlDeleteGrowableFunctionTable
 - winnt/RtlDeleteGrowableFunctionTable
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
 - ntdll.dll
 - API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
 - RtlDeleteGrowableFunctionTable
---

# RtlDeleteGrowableFunctionTable function


## -description

Informs the system that a previously reported dynamic function table is no longer in use.

## -parameters

### -param DynamicTable [in]

An opaque reference returned by <a href="/windows/desktop/api/winnt/nf-winnt-rtladdgrowablefunctiontable">RtlAddGrowableFunctionTable</a>.

## -returns

This function does not return a value.