---
UID: NF:pdh.PdhSetDefaultRealTimeDataSource
title: PdhSetDefaultRealTimeDataSource function (pdh.h)
description: Specifies the source of the real-time data.
helpviewer_keywords: ["DATA_SOURCE_REGISTRY","DATA_SOURCE_WBEM","PdhSetDefaultRealTimeDataSource","PdhSetDefaultRealTimeDataSource function [Perf]","_win32_pdhsetdefaultrealtimedatasource","base.pdhsetdefaultrealtimedatasource","pdh/PdhSetDefaultRealTimeDataSource","perf.pdhsetdefaultrealtimedatasource"]
old-location: perf\pdhsetdefaultrealtimedatasource.htm
tech.root: perf
ms.assetid: 5a46ac26-c1a1-40c1-a328-688e0b394e18
ms.date: 12/05/2018
ms.keywords: DATA_SOURCE_REGISTRY, DATA_SOURCE_WBEM, PdhSetDefaultRealTimeDataSource, PdhSetDefaultRealTimeDataSource function [Perf], _win32_pdhsetdefaultrealtimedatasource, base.pdhsetdefaultrealtimedatasource, pdh/PdhSetDefaultRealTimeDataSource, perf.pdhsetdefaultrealtimedatasource
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
 - PdhSetDefaultRealTimeDataSource
 - pdh/PdhSetDefaultRealTimeDataSource
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
 - PdhSetDefaultRealTimeDataSource
---

# PdhSetDefaultRealTimeDataSource function


## -description

Specifies the source of the real-time data.

## -parameters

### -param dwDataSourceId [in]

Source of the performance data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DATA_SOURCE_REGISTRY"></a><a id="data_source_registry"></a><dl>
<dt><b>DATA_SOURCE_REGISTRY</b></dt>
</dl>
</td>
<td width="60%">
The data source is the registry interface. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="DATA_SOURCE_WBEM"></a><a id="data_source_wbem"></a><dl>
<dt><b>DATA_SOURCE_WBEM</b></dt>
</dl>
</td>
<td width="60%">
The data source is a WMI provider.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following is a possible value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The parameter is not valid.

</td>
</tr>
</table>

## -remarks

The term <i>real-time</i> as used in the description of this function does not imply the standard meaning of the term <i>real-time</i>. Instead, it describes the collection of performance data from a source providing current information (for example, the registry or a WMI provider) rather than from a log file.

If you want to query real-time data from WMI, you must call <b>PdhSetDefaultRealTimeDataSource</b> to set the default real-time data source. You must call this function before calling any other PDH API function.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhselectdatasourcea">PdhSelectDataSource</a>