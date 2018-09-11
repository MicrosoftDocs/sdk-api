---
UID: NS:pdh._PDH_FMT_COUNTERVALUE
title: "_PDH_FMT_COUNTERVALUE"
author: windows-sdk-content
description: The PDH_FMT_COUNTERVALUE structure contains the computed value of the counter and its status.
old-location: perf\pdh_fmt_countervalue_str.htm
tech.root: perfctrs
ms.assetid: 68ccd722-94d2-4610-ba64-f51318f5436e
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PPDH_FMT_COUNTERVALUE, PDH_FMT_COUNTERVALUE, PDH_FMT_COUNTERVALUE structure [Perf], PPDH_FMT_COUNTERVALUE, PPDH_FMT_COUNTERVALUE structure pointer [Perf], _PDH_FMT_COUNTERVALUE, _win32_pdh_fmt_countervalue_str, base.pdh_fmt_countervalue_str, pdh/PDH_FMT_COUNTERVALUE, pdh/PPDH_FMT_COUNTERVALUE, perf.pdh_fmt_countervalue_str"
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
 - PDH_FMT_COUNTERVALUE
product: Windows
targetos: Windows
req.typenames: PDH_FMT_COUNTERVALUE, *PPDH_FMT_COUNTERVALUE
req.redist: 
---

# _PDH_FMT_COUNTERVALUE structure


## -description


The 
<b>PDH_FMT_COUNTERVALUE</b> structure contains the computed value of the counter and its status. 


## -struct-fields




### -field CStatus

Counter status that indicates if the counter value is valid. Check this member before using the data in a calculation or displaying its value. For a list of possible values, see 
<a href="https://msdn.microsoft.com/00ea5521-bc28-4a87-aba9-46c911631503">Checking PDH Interface Return Values</a>.


### -field longValue

The computed counter value as a <b>LONG</b>.


### -field doubleValue

The computed counter value as a <b>DOUBLE</b>.


### -field largeValue

The computed counter value as a <b>LONGLONG</b>.


### -field AnsiStringValue

The computed counter value as a <b>LPCSTR</b>. Not supported.


### -field WideStringValue

The computed counter value as a <b>LPCWSTR</b>. Not supported.


## -remarks



You specify the data type of the computed counter value when you call <a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> or <a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a> to compute the counter's value.




## -see-also




<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>
 

 

