---
UID: NF:pdh.PdhOpenQueryH
title: PdhOpenQueryH function (pdh.h)
description: Creates a new query that is used to manage the collection of performance data. This function is identical to the PdhOpenQuery function, except that it supports the use of handles to data sources.
helpviewer_keywords: ["PdhOpenQueryH","PdhOpenQueryH function [Perf]","_win32_pdhopenqueryh","base.pdhopenqueryh","pdh/PdhOpenQueryH","perf.pdhopenqueryh"]
old-location: perf\pdhopenqueryh.htm
tech.root: perf
ms.assetid: 068c55da-d7e0-4111-91c8-a2bbd676f99d
ms.date: 12/05/2018
ms.keywords: PdhOpenQueryH, PdhOpenQueryH function [Perf], _win32_pdhopenqueryh, base.pdhopenqueryh, pdh/PdhOpenQueryH, perf.pdhopenqueryh
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhOpenQueryH
 - pdh/PdhOpenQueryH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhOpenQueryH
---

# PdhOpenQueryH function


## -description

Creates a new query that is used to manage the collection of performance data.
			

This function is identical to 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function, except that it supports the use of handles to data sources.

## -parameters

### -param hDataSource [in]

Handle to a data source returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.

### -param dwUserData [in]

User-defined value to associate with this query. To retrieve the user data later, call 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a> function and access the <b>dwQueryUserData</b> member of <a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a>.

### -param phQuery [out]

Handle to the query. You use this handle in subsequent calls.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>