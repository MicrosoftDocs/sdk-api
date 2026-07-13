---
UID: NF:winevt.EvtOpenLog
title: EvtOpenLog function (winevt.h)
description: Gets a handle to a channel or log file that you can then use to get information about the channel or log file.
helpviewer_keywords: ["EvtOpenLog","EvtOpenLog function [EventLog]","wes.evtopenlog","winevt/EvtOpenLog"]
old-location: wes\evtopenlog.htm
tech.root: wes
ms.assetid: 1bf81452-2a62-4999-91b1-f1b42e6db91f
ms.date: 12/05/2018
ms.keywords: EvtOpenLog, EvtOpenLog function [EventLog], wes.evtopenlog, winevt/EvtOpenLog
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
 - EvtOpenLog
 - winevt/EvtOpenLog
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
 - EvtOpenLog
---

# EvtOpenLog function


## -description

Gets a handle to a channel or log file that you can then use to get information about the channel or log file.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to open a channel or log on the local computer.

### -param Path [in]

The name of the channel or the full path to the exported log file.

### -param Flags [in]

A flag that determines whether the <i>Path</i> parameter points to a log file or channel. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_open_log_flags">EVT_OPEN_LOG_FLAGS</a> enumeration.

## -returns

If successful, the function returns a handle to the file or channel; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

Relative paths and environment variables cannot be used when specifying a file.  A Universal Naming Convention (UNC) path can be used to locate the file.  Any relative path and environment variable expansion needs to be done prior to making API calls.

To get information about the channel or log file, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetloginfo">EvtGetLogInfo</a> function.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetloginfo">EvtGetLogInfo</a>