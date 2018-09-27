---
UID: NF:txlogpub.ILog.Force
title: ILog::Force
author: windows-sdk-content
description: Forces the contents of the log to disk, at least up through the specified LSN.
old-location: com\ilog_force.htm
tech.root: com
ms.assetid: 91df6049-37ce-4a46-b401-9af7d9c09f14
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Force, Force method [COM], Force method [COM],ILog interface, ILog interface [COM],Force method, ILog.Force, ILog::Force, _com_ilog_force, com.ilog_force, txlogpub/ILog::Force
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog.Force
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

