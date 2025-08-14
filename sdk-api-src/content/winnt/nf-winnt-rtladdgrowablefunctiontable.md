---
UID: NF:winnt.RtlAddGrowableFunctionTable
title: RtlAddGrowableFunctionTable function (winnt.h)
description: Informs the system of a dynamic function table representing a region of memory containing code.
helpviewer_keywords: ["RtlAddGrowableFunctionTable","RtlAddGrowableFunctionTable function","base.rtladdgrowablefunctiontable","winnt/RtlAddGrowableFunctionTable"]
old-location: base\rtladdgrowablefunctiontable.htm
tech.root: Debug
ms.assetid: 84ba7171-a4eb-4807-9883-f4fac6296ed0
ms.date: 12/05/2018
ms.keywords: RtlAddGrowableFunctionTable, RtlAddGrowableFunctionTable function, base.rtladdgrowablefunctiontable, winnt/RtlAddGrowableFunctionTable
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
 - RtlAddGrowableFunctionTable
 - winnt/RtlAddGrowableFunctionTable
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
 - RtlAddGrowableFunctionTable
---

# RtlAddGrowableFunctionTable function


## -description

Informs the system of a dynamic function table representing a region of memory containing 
    code.

## -parameters

### -param DynamicTable [out]

A pointer to a variable that receives an opaque reference to the newly-added table on success.

### -param FunctionTable

A pointer to a partially-filled array of 
       <a href="/windows/win32/api/winnt/ns-winnt-runtime_function">RUNTIME_FUNCTION</a> entries which provides 
       unwind information for the region of code. The entries in this array must remain sorted in ascending order of 
       the <b>BeginAddress</b> members.

### -param EntryCount [in]

The number of entries currently populated in the function table. This value may be zero.

### -param MaximumEntryCount [in]

The capacity of the function table.

### -param RangeBase [in]

The beginning of the memory range described by the function table.

### -param RangeEnd [in]

The end of the memory range described by the function table.

## -returns

This function returns zero on success. (More detail).

See 
      <a href="/openspecs/windows_protocols/ms-erref/596a1078-e883-4972-9bbc-49e60bebca55">http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx</a> 
      for a list of <b>NTSTATUS</b> values.

## -remarks

The function table can grow as code is added to the memory region. The entries in the table must be sorted. 
     This table is used for dispatching exceptions through runtime-generated code and for collecting stack 
     backtraces.