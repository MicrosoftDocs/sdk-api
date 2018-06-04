---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
       <a href="https://msdn.microsoft.com/9ed16f9a-3403-4ba9-9968-f51f6788a1f8">RUNTIME_FUNCTION</a> entries which provides 
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
      <a href="http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx">http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx</a> 
      for a list of <b>NTSTATUS</b> values.




## -remarks



The function table can grow as code is added to the memory region. The entries in the table must be sorted. 
     This table is used for dispatching exceptions through runtime-generated code and for collecting stack 
     backtraces.



