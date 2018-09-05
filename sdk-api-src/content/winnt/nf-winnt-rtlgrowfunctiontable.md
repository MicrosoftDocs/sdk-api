---
UID: NF:winnt.RtlGrowFunctionTable
title: RtlGrowFunctionTable function
author: windows-sdk-content
description: Reports that a dynamic function table has increased in size.
old-location: base\rtlgrowfunctiontable.htm
old-project: debug
ms.assetid: b917b732-4017-4365-b312-90bebfdd877b
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: RtlGrowFunctionTable, RtlGrowFunctionTable function, base.rtlgrowfunctiontable, winnt/RtlGrowFunctionTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
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
product: Windows
targetos: Windows
req.lib: Ntdll.lib
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlGrowFunctionTable function


## -description


Reports that a dynamic function table has increased in size. 


## -parameters




### -param DynamicTable

An opaque reference returned by <a href="https://msdn.microsoft.com/84ba7171-a4eb-4807-9883-f4fac6296ed0">RtlAddGrowableFunctionTable.</a>.


### -param NewEntryCount [in]

The new number of entries in the <a href="http://msdn.microsoft.com/en-us/library/ft9x1kdx">RUNTIME_FUNCTION</a> array. This must be greater than the previously reported size of the array.


## -returns



This function does not return a value.




## -remarks



<b>RtlGrowFunctionTable</b> should be called after populating the corresponding entries in the <a href="http://msdn.microsoft.com/en-us/library/ft9x1kdx">RUNTIME_FUNCTION</a> array specified in <a href="https://msdn.microsoft.com/84ba7171-a4eb-4807-9883-f4fac6296ed0">RtlAddGrowableFunctionTable.</a>




