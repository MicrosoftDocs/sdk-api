---
UID: NF:winevt.EvtGetLogInfo
title: EvtGetLogInfo function (winevt.h)
description: Gets information about a channel or log file.
helpviewer_keywords: ["EvtGetLogInfo","EvtGetLogInfo function [EventLog]","wes.evtgetloginfo","winevt/EvtGetLogInfo"]
old-location: wes\evtgetloginfo.htm
tech.root: wes
ms.assetid: 5261f367-3010-4b6d-9a53-77c908c867d4
ms.date: 12/05/2018
ms.keywords: EvtGetLogInfo, EvtGetLogInfo function [EventLog], wes.evtgetloginfo, winevt/EvtGetLogInfo
req.header: winevt.h
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtGetLogInfo
 - winevt/EvtGetLogInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
api_name:
 - EvtGetLogInfo
---

# EvtGetLogInfo function


## -description

Gets information about a channel or log file.

## -parameters

### -param Log [in]

 A handle to the channel or log file that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenlog">EvtOpenLog</a> function returns.

### -param PropertyId [in]

The identifier of the property to retrieve. For a list of property identifiers, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_log_property_id">EVT_LOG_PROPERTY_ID</a> enumeration.

### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.

### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the property value. The buffer contains an <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param PropertyValueBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

 You can get complete information for Operational and Admin channels or .evtx files; however, for Debug and Analytic channels or .etl files, you cannot get information for the EvtLogFull, EvtLogOldestRecordNumber, and EvtLogNumberOfLogRecords properties.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopenlog">EvtOpenLog</a>