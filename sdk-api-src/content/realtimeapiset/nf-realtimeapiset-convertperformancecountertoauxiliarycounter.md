---
UID: NF:realtimeapiset.ConvertPerformanceCounterToAuxiliaryCounter
title: ConvertPerformanceCounterToAuxiliaryCounter function (realtimeapiset.h)
description: Converts the specified performance counter value to the corresponding auxiliary counter value; optionally provides the estimated conversion error in nanoseconds due to latencies and maximum possible drift.
helpviewer_keywords: ["ConvertPerformanceCounterToAuxiliaryCounter","ConvertPerformanceCounterToAuxiliaryCounter function","base.convertperformancecountertoauxiliarycounter","realtimeapiset/ConvertPerformanceCounterToAuxiliaryCounter"]
old-location: base\convertperformancecountertoauxiliarycounter.htm
tech.root: winprog
ms.assetid: 2499981B-6C13-4A3D-836A-D4CCD11C8D50
ms.date: 12/05/2018
ms.keywords: ConvertPerformanceCounterToAuxiliaryCounter, ConvertPerformanceCounterToAuxiliaryCounter function, base.convertperformancecountertoauxiliarycounter, realtimeapiset/ConvertPerformanceCounterToAuxiliaryCounter
req.header: realtimeapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConvertPerformanceCounterToAuxiliaryCounter
 - realtimeapiset/ConvertPerformanceCounterToAuxiliaryCounter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-realtime-l1-1-2.dll
 - Kernel32.dll
api_name:
 - ConvertPerformanceCounterToAuxiliaryCounter
---

# ConvertPerformanceCounterToAuxiliaryCounter function


## -description

Converts the specified performance counter value to the corresponding auxiliary counter value; optionally provides the estimated conversion error in nanoseconds due to latencies and maximum possible drift.

## -parameters

### -param ullPerformanceCounterValue [in]

The performance counter value to convert.

### -param lpAuxiliaryCounterValue [out]

On success, contains the converted auxiliary counter value. Will be undefined if the function fails.

### -param lpConversionError [out, optional]

On success, contains the estimated conversion error, in nanoseconds. Will be undefined if the function fails.

## -returns

Returns <b>S_OK</b> if the conversion succeeds; otherwise, returns another <b>HRESULT</b> specifying the error. 

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The auxiliary counter is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The value to convert is outside the permitted range (+/- 10 seconds from when the called occurred).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The value to convert is prior to the last system boot or S3/S4 transition.

</td>
</tr>
</table>

