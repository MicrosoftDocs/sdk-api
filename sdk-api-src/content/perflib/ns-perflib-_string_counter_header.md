---
UID: NS:perflib._STRING_COUNTER_HEADER
title: "_STRING_COUNTER_HEADER"
author: windows-sdk-content
description: Indicates where in the PERF_STRING_BUFFER_HEADER block that the string that contains the name or help string for the indicated performance counter starts.
old-location: perf\perf_string_counter_header.htm
tech.root: perfctrs
ms.assetid: 73DFA1C0-B0E8-4788-8CBA-1CFA7580F633
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PPERF_STRING_COUNTER_HEADER, PERF_STRING_COUNTER_HEADER, PERF_STRING_COUNTER_HEADER structure [Perf], PPERF_STRING_COUNTER_HEADER, PPERF_STRING_COUNTER_HEADER structure pointer [Perf], _STRING_COUNTER_HEADER, perf.perf_string_counter_header, perflib/PERF_STRING_COUNTER_HEADER, perflib/PPERF_STRING_COUNTER_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - PERF_STRING_COUNTER_HEADER
product: Windows
targetos: Windows
req.typenames: PERF_STRING_COUNTER_HEADER, *PPERF_STRING_COUNTER_HEADER
req.redist: 
---

# _STRING_COUNTER_HEADER structure


## -description


Indicates where in the <a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block that the string that contains the name or help string  for the indicated performance counter starts. The <b>PERF_STRING_COUNTER_HEADER</b> structure is part of the
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block


## -struct-fields




### -field dwCounterId

The identifier of the  performance counter.


### -field dwOffset

The number of bytes from the start of the
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block to the null-terminated UTF-16LE data. A value of 0xFFFFFFFF indicates that the string is not present; in other words, that the value of the string is NULL.


## -remarks



The <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTER_NAME_STRINGS</b> or <b>PERF_REG_COUNTER_HELP_STRINGS</b> gets a
<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block that contains one or more
<b>PERF_STRING_COUNTER_HEADER</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a>



<a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a>
 

 

