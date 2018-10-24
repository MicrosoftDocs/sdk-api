---
UID: NF:perflib.PerfSetULongCounterValue
title: PerfSetULongCounterValue function
author: windows-sdk-content
description: Updates the value of a counter whose value is a 4-byte unsigned integer. Providers use this function.
old-location: perf\perfsetulongcountervalue.htm
tech.root: perfctrs
ms.assetid: b790bea0-90d8-4894-bacb-a27f777cf240
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: PerfSetULongCounterValue, PerfSetULongCounterValue function [Perf], base.perfsetulongcountervalue, perf.perfsetulongcountervalue, perflib/PerfSetULongCounterValue
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
 - PerfSetULongCounterValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfSetULongCounterValue function


## -description


Updates the value of a counter whose value is a 4-byte unsigned integer.  Providers use this function.


## -parameters




### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/10112f43-f483-4ecb-aa7d-60efaad149c6">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


### -param Instance [in]

A <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance. The <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a> function returns this pointer.


### -param CounterId [in]

Identifier that uniquely identifies the counter to update in the instance block. The identifier is defined in the <b>id</b> attribute of the <a href="perf.counter_element">counter</a> element and must match the <b>CounterId</b> member of one of the <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> structures in the instance block. Use the counter ID constant that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the constant, see the <b>symbol</b> attribute of the <b>counter</b> element.

<b>Windows Vista:  </b>The counter ID constant is not available.


### -param Value [in]

New 4-byte counter value.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



This is a convenience function for setting raw counter data. To update the raw counter data yourself, use the <b>Offset</b> member of the <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> structure to access the raw counter data for a specific counter. The <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure block contains one or more counter information structures.

You can use the <a href="https://msdn.microsoft.com/002162a0-d782-4648-949e-178985fd1d44">PerfIncrementULongCounterValue</a> and <a href="https://msdn.microsoft.com/5e8b40d6-b794-4bac-8832-3eb14c49ecec">PerfDecrementULongCounterValue</a> functions to increment or decrement the counter value, respectively.




## -see-also




<a href="https://msdn.microsoft.com/5e8b40d6-b794-4bac-8832-3eb14c49ecec">PerfDecrementULongCounterValue</a>



<a href="https://msdn.microsoft.com/002162a0-d782-4648-949e-178985fd1d44">PerfIncrementULongCounterValue</a>



<a href="https://msdn.microsoft.com/0694ff8c-4c36-4bf7-a2b3-c032bf7a2f65">PerfSetCounterRefValue</a>



<a href="https://msdn.microsoft.com/c38f9efc-7ea8-4841-9a31-a88d4f87369c">PerfSetULongLongCounterValue</a>
 

 

