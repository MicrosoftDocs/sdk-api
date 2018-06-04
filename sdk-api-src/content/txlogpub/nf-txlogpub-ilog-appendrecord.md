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

# ILog::AppendRecord


## -description


Write a new record to the end of the log.


## -parameters




### -param rgBlob [in]

A pointer to an array of BLOBs of data to be written.


### -param cBlob [in]

The size of the <i>rgBlob</i> array, in elements.


### -param fForceNow [in]

Indicates whether to force the data to disk. If <b>TRUE</b>, the contents of the log up to this record must be forced to disk before the call returns. If <b>FALSE</b>, this record may be buffered in memory to be written after the call returns successfully.


### -param plsn [in, out]

A pointer to the LSN of the newly appended record. If the LSN of the newly appended record is not needed, this parameter can be <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each log record written or read by <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> is an opaque BLOB of data. As a convenience to callers, <b>AppendRecord</b> allows multiple BLOBs to be concatenated into a single record; because many implementations of <b>ILog</b> will copy records to a buffer in memory, it may be inefficient for the caller to allocate memory for concatenating the parts of a record. However, once a record is appended to the log, <b>ILog</b> provides no method to extract individual BLOBs from the record. It is the responsibility of the caller to parse the data in records read from the log. See <a href="https://msdn.microsoft.com/756d56a4-083f-45cd-bcdc-7c8a15dabae6">ILog::ReadRecord</a>.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A failure return value indicates that any records appended to the log since the last time it was successfully forced are not guaranteed to be on disk. The <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> interface does not provide a method to determine which records have been successfully written to disk. If you need to know which records were successfully written to disk, you must force the log for each record.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If <i>fForceNow</i> is <b>TRUE</b>, it is recommended that you flush file buffers (for example, using the <a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a> function) before returning from this method.




## -see-also




<a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a>



<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>
 

 

