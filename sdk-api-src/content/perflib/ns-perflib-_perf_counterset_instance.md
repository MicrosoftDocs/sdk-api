---
UID: NS:perflib._PERF_COUNTERSET_INSTANCE
title: "_PERF_COUNTERSET_INSTANCE"
author: windows-sdk-content
description: Defines an instance of a counter set.
old-location: perf\perf_counterset_instance.htm
tech.root: perfctrs
ms.assetid: 709d5339-cedd-4b03-9d8e-c125eb3bcac0
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PPERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE structure [Perf], PERF_COUNTERSET_INSTANCE,*PPERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE,*PPERF_COUNTERSET_INSTANCE structure [Perf], _PERF_COUNTERSET_INSTANCE, base.perf_counterset_instance, perf.perf_counterset_instance, perflib/PERF_COUNTERSET_INSTANCE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTERSET_INSTANCE, *PPERF_COUNTERSET_INSTANCE
product: Windows
targetos: Windows
req.typenames: PERF_COUNTERSET_INSTANCE, *PPERF_COUNTERSET_INSTANCE
req.redist: 
---

# _PERF_COUNTERSET_INSTANCE structure


## -description


Defines an instance of a counter set. 


## -struct-fields




### -field CounterSetGuid

GUID that identifies the counter set to which this instance belongs.


### -field dwSize

Size, in bytes, of the instance block. The instance block contains this structure, followed by one or more <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> blocks, and ends with the instance name.


### -field InstanceId

Identifier that uniquely identifies this instance. 

The provider specified the identifier when calling <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>.


### -field InstanceNameOffset

Byte offset from the beginning of this structure to the null-terminated Unicode instance name.

The provider specified the instance name when calling <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>.


### -field InstanceNameSize

Size, in bytes, of the instance name. The size includes the null-terminator.


## -remarks



The <b>Offset</b> member of  <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> contains the byte offset from the beginning of the <b>PERF_COUNTERSET_INSTANCE</b> block to the counter's raw counter value.




## -see-also




<a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a>



<a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>



<a href="https://msdn.microsoft.com/8266e58c-c0a3-42dd-9f06-0d04dccfcf7c">PerfDeleteInstance</a>



<a href="https://msdn.microsoft.com/844f3f9e-8de2-4995-b13c-befe0da8a1ab">PerfQueryInstance</a>
 

 

