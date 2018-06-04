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

# PerfSetULongLongCounterValue function


## -description


Updates the value of a counter whose value is an 8-byte unsigned integer. Providers use this function.


## -parameters




### -param Provider

TBD


### -param Instance

TBD


### -param CounterId [in]

Identifier that uniquely identifies the counter to update in the instance block. The identifier is defined in the <b>id</b> attribute of the <a href="https://msdn.microsoft.com/">counter</a> element and must match the <b>CounterId</b> member of one of the <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> structures in the instance block. Use the counter ID constant that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the constant, see the <b>symbol</b> attribute of the <b>counter</b> element.

<b>Windows Vista:  </b>The counter ID constant is not available.


### -param Value

TBD




#### - hProvider [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


#### - llValue [in]

New 8-byte counter value.


#### - pInstance [in]

A <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance. The <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a> function returns this pointer.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



This is a convenience function for setting raw counter data. To update the raw counter data yourself, use the <b>Offset</b> member of the <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> structure to access the raw counter data for a specific counter. The <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure block contains one or more counter information structures.

You can use the <a href="https://msdn.microsoft.com/6e701561-4036-4ae4-8d4e-667fa6a20d99">PerfIncrementULongLongCounterValue</a> and <a href="https://msdn.microsoft.com/38fd52a7-c2af-4c69-a104-aba6a602fbf4">PerfDecrementULongLongCounterValue</a> functions to increment or decrement the counter value, respectively.




## -see-also




<a href="https://msdn.microsoft.com/38fd52a7-c2af-4c69-a104-aba6a602fbf4">PerfDecrementULongLongCounterValue</a>



<a href="https://msdn.microsoft.com/6e701561-4036-4ae4-8d4e-667fa6a20d99">PerfIncrementULongLongCounterValue</a>



<a href="https://msdn.microsoft.com/0694ff8c-4c36-4bf7-a2b3-c032bf7a2f65">PerfSetCounterRefValue</a>



<a href="https://msdn.microsoft.com/b790bea0-90d8-4894-bacb-a27f777cf240">PerfSetULongCounterValue</a>
 

 

