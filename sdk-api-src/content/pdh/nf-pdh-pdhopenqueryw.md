---
UID: NF:pdh.PdhOpenQueryW
title: PdhOpenQueryW function (pdh.h)
description: Creates a new query that is used to manage the collection of performance data. To use handles to data sources, use the PdhOpenQueryH function. (Unicode)
helpviewer_keywords: ["PdhOpenQuery", "PdhOpenQuery function [Perf]", "PdhOpenQueryW", "_win32_pdhopenquery", "base.pdhopenquery", "pdh/PdhOpenQuery", "pdh/PdhOpenQueryW", "perf.pdhopenquery"]
old-location: perf\pdhopenquery.htm
tech.root: perf
ms.assetid: ec4e5353-c7f5-4957-b7f4-39df508846a0
ms.date: 12/05/2018
ms.keywords: PdhOpenQuery, PdhOpenQuery function [Perf], PdhOpenQueryA, PdhOpenQueryW, _win32_pdhopenquery, base.pdhopenquery, pdh/PdhOpenQuery, pdh/PdhOpenQueryA, pdh/PdhOpenQueryW, perf.pdhopenquery
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhOpenQueryW (Unicode) and PdhOpenQueryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhOpenQueryW
 - pdh/PdhOpenQueryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-eventing-pdh-l1-1-3.dll
 - ext-ms-win-eventing-pdh-l1-1-2.dll
 - ext-ms-win-eventing-pdh-l1-1-1.dll
 - ext-ms-win-eventing-pdh-l1-1-0.dll
 - Pdh.dll
api_name:
 - PdhOpenQuery
 - PdhOpenQueryA
 - PdhOpenQueryW
---

# PdhOpenQueryW function


## -description

Creates a new query that is used to manage the collection of performance data.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenqueryh">PdhOpenQueryH</a> function.

## -parameters

### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of the log file from which to retrieve performance data. If <b>NULL</b>, performance data is collected from a real-time data source.

### -param dwUserData [in]

User-defined value to associate with this query. To retrieve the user data later, call 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a> and access the <b>dwQueryUserData</b> member of <a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a>.

### -param phQuery [out]

Handle to the query. You use this handle in subsequent calls.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhclosequery">PdhCloseQuery</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhisrealtimequery">PdhIsRealTimeQuery</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenqueryh">PdhOpenQueryH</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhsetdefaultrealtimedatasource">PdhSetDefaultRealTimeDataSource</a>

## -remarks

> [!NOTE]
> The pdh.h header defines PdhOpenQuery as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
