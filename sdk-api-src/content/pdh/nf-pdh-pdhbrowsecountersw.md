---
UID: NF:pdh.PdhBrowseCountersW
title: PdhBrowseCountersW function (pdh.h)
description: Displays a Browse Counters dialog box that the user can use to select one or more counters that they want to add to the query. To use handles to data sources, use the PdhBrowseCountersH function. (Unicode)
helpviewer_keywords: ["PdhBrowseCounters", "PdhBrowseCounters function [Perf]", "PdhBrowseCountersW", "_win32_pdhbrowsecounters", "base.pdhbrowsecounters", "pdh/PdhBrowseCounters", "pdh/PdhBrowseCountersW", "perf.pdhbrowsecounters"]
old-location: perf\pdhbrowsecounters.htm
tech.root: perf
ms.assetid: 4e9e4b20-a573-4f6d-97e8-63bcc675032b
ms.date: 12/05/2018
ms.keywords: PdhBrowseCounters, PdhBrowseCounters function [Perf], PdhBrowseCountersA, PdhBrowseCountersW, _win32_pdhbrowsecounters, base.pdhbrowsecounters, pdh/PdhBrowseCounters, pdh/PdhBrowseCountersA, pdh/PdhBrowseCountersW, perf.pdhbrowsecounters
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhBrowseCountersW (Unicode) and PdhBrowseCountersA (ANSI)
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
 - PdhBrowseCountersW
 - pdh/PdhBrowseCountersW
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
 - PdhBrowseCounters
 - PdhBrowseCountersA
 - PdhBrowseCountersW
---

# PdhBrowseCountersW function


## -description

Displays a  <b>Browse Counters</b> dialog box that the user can use to select one or more counters that they want to add to the query.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersha">PdhBrowseCountersH</a> function.

## -parameters

### -param pBrowseDlgData [in]

A 
<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a> structure that specifies the behavior of the dialog box.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

## -remarks

Note that the dialog
   box can return PDH_DIALOG_CANCELLED if <b>bSingleCounterPerDialog</b> is <b>FALSE</b> and the user clicks the  <b>Close</b> button, so your error handling would have to account for this.

For information on using this function, see <a href="/windows/desktop/PerfCtrs/browsing-counters">Browsing Counters</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/browsing-performance-counters">Browsing Performance Counters</a>.

<div class="code"></div>




> [!NOTE]
> The pdh.h header defines PdhBrowseCounters as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nc-pdh-counterpathcallback">CounterPathCallBack</a>



<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersha">PdhBrowseCountersH</a>
