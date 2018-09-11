---
UID: NF:perflib.PerfCreateInstance
title: PerfCreateInstance function
author: windows-sdk-content
description: Creates an instance of the specified counter set.
old-location: perf\perfcreateinstance.htm
tech.root: perfctrs
ms.assetid: 73be8588-2c87-4c27-933d-62b8605ed9a3
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: PerfCreateInstance, PerfCreateInstance function [Perf], base.perfcreateinstance, perf.perfcreateinstance, perflib/PerfCreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-perfcounters-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PerfCreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfCreateInstance function


## -description


Creates an instance of the specified counter set. Providers use this function.


## -parameters




### -param ProviderHandle [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/10112f43-f483-4ecb-aa7d-60efaad149c6">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


### -param CounterSetGuid [in]

GUID that uniquely identifies the counter set that you want to create an instance of. This is the same GUID specified in the <b>guid</b> attribute of the <a href="https://msdn.microsoft.com/library/Ee781342(v=VS.85).aspx">counterSet</a> element. Use the GUID variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <b>counterSet</b> element.

<b>Windows Vista:  </b>The GUID variable is not available.


### -param Name [in]

<b>Null</b>-terminated Unicode string that contains a unique name for this instance. 


### -param Id [in]

Unique identifier for this instance of the counter set. The identifier can be a serial number that you increment for each new instance.


## -returns



A <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure that contains the instance of the counter set or <b>NULL</b> if PERFLIB could not create the instance. Cache this pointer to use in later calls instead of calling <a href="https://msdn.microsoft.com/844f3f9e-8de2-4995-b13c-befe0da8a1ab">PerfQueryInstance</a> to retrieve the pointer to the instance.

This function returns <b>NULL</b> if an error occurred. To determine the error that occurred, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The provider determines when it creates an instance. If the counter data is more static, the provider can create an instance at initialization time. For example, the number of processors on a computer would be considered static, so a provider that provides counter data for processors could create an instance for each processor on the computer at initialization time. For counters that are more dynamic, such as disk or process counters, the providers would create the new instances in response to a new USB device being added or a new process being created.

When the provider calls this function, PERFLIB allocates local memory for the new instance and builds the instance block. PERFLIB deletes the memory when the provider calls the <a href="https://msdn.microsoft.com/8266e58c-c0a3-42dd-9f06-0d04dccfcf7c">PerfDeleteInstance</a> function.

The instance contains the raw counter data. Providers use the following three functions to update the raw counter data:

<ul>
<li>
<a href="https://msdn.microsoft.com/b790bea0-90d8-4894-bacb-a27f777cf240">PerfSetUlongCounterValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c38f9efc-7ea8-4841-9a31-a88d4f87369c">PerfSetUlongLongCounterValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0694ff8c-4c36-4bf7-a2b3-c032bf7a2f65">PerfSetCounterRefValue</a>
</li>
</ul>
Typically, the provider keeps the counter data up-to-date at all times. As an alternative, the provider can implement the <a href="https://msdn.microsoft.com/0f771ab7-af42-481b-b2da-20dcdf49b82b">ControlCallback</a> function and use the <b>PERF_COLLECT_START</b> request code to trigger the updates.




## -see-also




<a href="https://msdn.microsoft.com/8266e58c-c0a3-42dd-9f06-0d04dccfcf7c">PerfDeleteInstance</a>



<a href="https://msdn.microsoft.com/844f3f9e-8de2-4995-b13c-befe0da8a1ab">PerfQueryInstance</a>
 

 

