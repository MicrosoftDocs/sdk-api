---
UID: NS:pdh._PDH_RAW_COUNTER
title: "_PDH_RAW_COUNTER"
author: windows-sdk-content
description: The PDH_RAW_COUNTER structure returns the data as it was collected from the counter provider. No translation, formatting, or other interpretation is performed on the data.
old-location: perf\pdh_raw_counter_str.htm
tech.root: perfctrs
ms.assetid: 237a3c82-0ab4-45cb-bd93-2f308178c573
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PPDH_RAW_COUNTER, PDH_RAW_COUNTER, PDH_RAW_COUNTER structure [Perf], PPDH_RAW_COUNTER, PPDH_RAW_COUNTER structure pointer [Perf], _PDH_RAW_COUNTER, _win32_pdh_raw_counter_str, base.pdh_raw_counter_str, pdh/PDH_RAW_COUNTER, pdh/PPDH_RAW_COUNTER, perf.pdh_raw_counter_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Pdh.h
api_name:
 - PDH_RAW_COUNTER
product: Windows
targetos: Windows
req.typenames: PDH_RAW_COUNTER, *PPDH_RAW_COUNTER
req.redist: 
---

# _PDH_RAW_COUNTER structure


## -description


The 
<b>PDH_RAW_COUNTER</b> structure returns the data as it was collected from the counter provider. No translation, formatting, or other interpretation is performed on the data.
		


## -struct-fields




### -field CStatus

Counter status that indicates if the counter value is valid. Check this member before using the data in a calculation or displaying its value. For a list of possible values, see 
<a href="https://msdn.microsoft.com/00ea5521-bc28-4a87-aba9-46c911631503">Checking PDH Interface Return Values</a>.


### -field TimeStamp

Local time for when the data was collected, in 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.


### -field FirstValue

First raw counter value.


### -field SecondValue

Second raw counter value. Rate counters require two values in order to compute a displayable value.


### -field MultiCount

If the counter type contains the PERF_MULTI_COUNTER flag, this member contains the additional counter data used in the calculation. For example, the PERF_100NSEC_MULTI_TIMER counter type contains the PERF_MULTI_COUNTER flag.


## -see-also




<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/a986ae6c-88ee-4a03-9077-3d286157b9d1">PdhComputeCounterStatistics</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>
 

 

