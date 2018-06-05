---
UID: NF:winnt.RtlDeleteGrowableFunctionTable
title: RtlDeleteGrowableFunctionTable function
author: windows-sdk-content
description: Informs the system that a previously reported dynamic function table is no longer in use.
old-location: base\rtldeletegrowablefunctiontable.htm
old-project: Debug
ms.assetid: 2ae4eef2-5cdc-4ebf-9285-ef6a1a4e9197
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: RtlDeleteGrowableFunctionTable, RtlDeleteGrowableFunctionTable function, base.rtldeletegrowablefunctiontable, winnt/RtlDeleteGrowableFunctionTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ntdll.dll
-	API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
-	RtlDeleteGrowableFunctionTable
product: Windows
targetos: Windows
req.lib: Ntdll.lib
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlDeleteGrowableFunctionTable function


## -description


Informs the system that a previously reported dynamic function table is no longer in use.


## -parameters




### -param DynamicTable [in]

An opaque reference returned by <a href="https://msdn.microsoft.com/84ba7171-a4eb-4807-9883-f4fac6296ed0">RtlAddGrowableFunctionTable.</a>



## -returns



This function does not return a value.



