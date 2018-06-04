---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _EVT_LOG_PROPERTY_ID enumeration


## -description


Defines the identifiers that identify the log file metadata properties of a channel or log file.


## -enum-fields




### -field EvtLogCreationTime

Identifies the property that contains the time that the channel or log file was created. The variant type for this property is <b>EvtVarTypeFileTime</b>.


### -field EvtLogLastAccessTime

Identifies the property that contains the last time that the channel or log file was accessed. The variant type for this property is <b>EvtVarTypeFileTime</b>.


### -field EvtLogLastWriteTime

Identifies the property that contains the last time that the channel or log file was written to. The variant type for this property is <b>EvtVarTypeFileTime</b>.


### -field EvtLogFileSize

Identifies the property that contains the size of the file, in bytes. The variant type for this property is <b>EvtVarTypeUInt64</b>.


### -field EvtLogAttributes

Identifies the property that contains the file attributes (for details on the file attributes, see the <a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a> function). The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtLogNumberOfLogRecords

Identifies the property that contains the number of records in the channel or log file. The variant type for this property is <b>EvtVarTypeUInt64</b>.


### -field EvtLogOldestRecordNumber

Identifies the property that contains the record number of the oldest event in the channel or log file. The variant type for this property is <b>EvtVarTypeUInt64</b>.


### -field EvtLogFull

Identifies the property that you use to determine whether the channel or log file is full. The variant type for this property is <b>EvtVarTypeBoolean</b>. The channel is full if another event cannot be written to the channel (for example, if the channel is sequential and maximum size is reached). The property will always be false if the channel is circular or the sequential log is automatically backed up.


## -see-also




<a href="https://msdn.microsoft.com/5261f367-3010-4b6d-9a53-77c908c867d4">EvtGetLogInfo</a>
 

 

