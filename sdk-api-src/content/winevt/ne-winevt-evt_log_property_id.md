---
UID: NE:winevt._EVT_LOG_PROPERTY_ID
title: EVT_LOG_PROPERTY_ID (winevt.h)
description: Defines the identifiers that identify the log file metadata properties of a channel or log file.
helpviewer_keywords: ["EVT_LOG_PROPERTY_ID","EVT_LOG_PROPERTY_ID enumeration [EventLog]","EvtLogAttributes","EvtLogCreationTime","EvtLogFileSize","EvtLogFull","EvtLogLastAccessTime","EvtLogLastWriteTime","EvtLogNumberOfLogRecords","EvtLogOldestRecordNumber","wes.evt_log_property_id","winevt/EVT_LOG_PROPERTY_ID","winevt/EvtLogAttributes","winevt/EvtLogCreationTime","winevt/EvtLogFileSize","winevt/EvtLogFull","winevt/EvtLogLastAccessTime","winevt/EvtLogLastWriteTime","winevt/EvtLogNumberOfLogRecords","winevt/EvtLogOldestRecordNumber"]
old-location: wes\evt_log_property_id.htm
tech.root: wes
ms.assetid: c5b8b80b-6549-497a-adc3-2517bd5f27c7
ms.date: 12/05/2018
ms.keywords: EVT_LOG_PROPERTY_ID, EVT_LOG_PROPERTY_ID enumeration [EventLog], EvtLogAttributes, EvtLogCreationTime, EvtLogFileSize, EvtLogFull, EvtLogLastAccessTime, EvtLogLastWriteTime, EvtLogNumberOfLogRecords, EvtLogOldestRecordNumber, wes.evt_log_property_id, winevt/EVT_LOG_PROPERTY_ID, winevt/EvtLogAttributes, winevt/EvtLogCreationTime, winevt/EvtLogFileSize, winevt/EvtLogFull, winevt/EvtLogLastAccessTime, winevt/EvtLogLastWriteTime, winevt/EvtLogNumberOfLogRecords, winevt/EvtLogOldestRecordNumber
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVT_LOG_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_LOG_PROPERTY_ID
 - winevt/_EVT_LOG_PROPERTY_ID
 - EVT_LOG_PROPERTY_ID
 - winevt/EVT_LOG_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_LOG_PROPERTY_ID
---

# EVT_LOG_PROPERTY_ID enumeration


## -description

Defines the identifiers that identify the log file metadata properties of a channel or log file.

## -enum-fields

### -field EvtLogCreationTime:0

Identifies the property that contains the time that the channel or log file was created. The variant type for this property is <b>EvtVarTypeFileTime</b>.

### -field EvtLogLastAccessTime

Identifies the property that contains the last time that the channel or log file was accessed. The variant type for this property is <b>EvtVarTypeFileTime</b>.

### -field EvtLogLastWriteTime

Identifies the property that contains the last time that the channel or log file was written to. The variant type for this property is <b>EvtVarTypeFileTime</b>.

### -field EvtLogFileSize

Identifies the property that contains the size of the file, in bytes. The variant type for this property is <b>EvtVarTypeUInt64</b>.

### -field EvtLogAttributes

Identifies the property that contains the file attributes (for details on the file attributes, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> function). The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EvtLogNumberOfLogRecords

Identifies the property that contains the number of records in the channel or log file. The variant type for this property is <b>EvtVarTypeUInt64</b>.

### -field EvtLogOldestRecordNumber

Identifies the property that contains the record number of the oldest event in the channel or log file. The variant type for this property is <b>EvtVarTypeUInt64</b>.

### -field EvtLogFull

Identifies the property that you use to determine whether the channel or log file is full. The variant type for this property is <b>EvtVarTypeBoolean</b>. The channel is full if another event cannot be written to the channel (for example, if the channel is sequential and maximum size is reached). The property will always be false if the channel is circular or the sequential log is automatically backed up.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetloginfo">EvtGetLogInfo</a>
