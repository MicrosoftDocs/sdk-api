---
UID: NF:pdh.PdhBrowseCountersHA
title: PdhBrowseCountersHA function (pdh.h)
description: Displays a Browse Counters dialog box that the user can use to select one or more counters that they want to add to the query. This function is identical to the PdhBrowseCounters function, except that it supports the use of handles to data sources.
helpviewer_keywords: ["PdhBrowseCountersH","PdhBrowseCountersH function [Perf]","PdhBrowseCountersHA","PdhBrowseCountersHW","_win32_pdhbrowsecountersh","base.pdhbrowsecountersh","pdh/PdhBrowseCountersH","pdh/PdhBrowseCountersHA","pdh/PdhBrowseCountersHW","perf.pdhbrowsecountersh"]
old-location: perf\pdhbrowsecountersh.htm
tech.root: perfctrs
ms.assetid: ab835bf8-1adc-463f-99c3-654a328af98a
ms.date: 12/05/2018
ms.keywords: PdhBrowseCountersH, PdhBrowseCountersH function [Perf], PdhBrowseCountersHA, PdhBrowseCountersHW, _win32_pdhbrowsecountersh, base.pdhbrowsecountersh, pdh/PdhBrowseCountersH, pdh/PdhBrowseCountersHA, pdh/PdhBrowseCountersHW, perf.pdhbrowsecountersh
f1_keywords:
- pdh/PdhBrowseCountersH
dev_langs:
- c++
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhBrowseCountersHW (Unicode) and PdhBrowseCountersHA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Pdh.dll
api_name:
- PdhBrowseCountersH
- PdhBrowseCountersHA
- PdhBrowseCountersHW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhBrowseCountersHA function


## -description


Displays a <b>Browse Counters</b> dialog box that the user can use to select one or more counters that they want to add to the query. 
			

This function is identical to 
the <a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersa">PdhBrowseCounters</a> function, except that it supports the use of handles to data sources.


## -parameters




### -param pBrowseDlgData [in]

A 
<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha">PDH_BROWSE_DLG_CONFIG_H</a> structure that specifies the behavior of the dialog box.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.




## -remarks



Note that the dialog
   box can return PDH_DIALOG_CANCELLED if <b>bSingleCounterPerDialog</b>is <b>FALSE</b> and the user clicks the <b>Close</b> button, so your error handling would have to account for this.




## -see-also




<a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha">PDH_BROWSE_DLG_CONFIG_H</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenummachinesha">PdhEnumMachinesH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenumobjectitemsha">PdhEnumObjectItemsH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpathha">PdhExpandWildCardPathH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangeh">PdhGetDataSourceTimeRangeH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfcounterha">PdhGetDefaultPerfCounterH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfobjectha">PdhGetDefaultPerfObjectH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenqueryh">PdhOpenQueryH</a>
 

 

