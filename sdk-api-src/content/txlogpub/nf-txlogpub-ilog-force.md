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

# ILog::Force


## -description


Forces the contents of the log to disk, at least up through the specified LSN.


## -parameters




### -param lsnMinToForce [in]

At the very least, all records that have not yet been written to disk with an LSN less than or equal to <i>lsnMinToForce</i> must be written to disk now. An implementation may, however, choose to write more records than what is strictly required. For example, an implementation is allowed to force all records to disk, regardless of the value of <i>lsnMinToForce</i>. Passing 0 as <i>lsnMinToForce</i> indicates that the entire log is to be forced to disk.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The log may also be forced to disk after appending individual records. See <a href="https://msdn.microsoft.com/e739acb5-4d93-4871-8b35-54d45138fe0f">ILog::AppendRecord</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A failure return value indicates that any records appended to the log since the last time it was successfully forced are not guaranteed to be on disk. The <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> interface does not provide a method to determine which records have been successfully written to disk. If you need to know which records were successfully written to disk, you must force the log for each record. See <a href="https://msdn.microsoft.com/e739acb5-4d93-4871-8b35-54d45138fe0f">ILog::AppendRecord</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
It is recommended that you flush file buffers (for example, using the <a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a> function) before returning from this method.




## -see-also




<a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a>



<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>
 

 

