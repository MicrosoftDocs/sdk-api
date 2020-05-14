---
UID: NF:winnt.RtlGrowFunctionTable
title: RtlGrowFunctionTable function (winnt.h)
description: Reports that a dynamic function table has increased in size.helpviewer_keywords: ["RtlGrowFunctionTable","RtlGrowFunctionTable function","base.rtlgrowfunctiontable","winnt/RtlGrowFunctionTable"]
old-location: base\rtlgrowfunctiontable.htm
tech.root: Debug
ms.assetid: b917b732-4017-4365-b312-90bebfdd877b
ms.date: 12/05/2018
ms.keywords: RtlGrowFunctionTable, RtlGrowFunctionTable function, base.rtlgrowfunctiontable, winnt/RtlGrowFunctionTable
f1_keywords:
- winnt/RtlGrowFunctionTable
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ntdll.dll
- API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
- RtlGrowFunctionTable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtlGrowFunctionTable function


## -description


Reports that a dynamic function table has increased in size. 


## -parameters




### -param DynamicTable

An opaque reference returned by <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-rtladdgrowablefunctiontable">RtlAddGrowableFunctionTable.</a>.


### -param NewEntryCount [in]

The new number of entries in the <a href="https://docs.microsoft.com/cpp/build/struct-runtime-function">RUNTIME_FUNCTION</a> array. This must be greater than the previously reported size of the array.


## -returns



This function does not return a value.




## -remarks



<b>RtlGrowFunctionTable</b> should be called after populating the corresponding entries in the <a href="https://docs.microsoft.com/cpp/build/struct-runtime-function">RUNTIME_FUNCTION</a> array specified in <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-rtladdgrowablefunctiontable">RtlAddGrowableFunctionTable.</a>




