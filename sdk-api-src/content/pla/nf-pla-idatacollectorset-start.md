---
UID: NF:pla.IDataCollectorSet.Start
title: IDataCollectorSet::Start method
author: windows-driver-content
description: Manually starts the data collector set.
old-location: pla\idatacollectorset_start.htm
old-project: PLA
ms.assetid: 63f0c7b7-0dc6-4491-a2f5-eaae9d22da61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataCollectorSet, IDataCollectorSet interface [PLA], Start method, IDataCollectorSet::Start, Start method [PLA], Start method [PLA], IDataCollectorSet interface, Start,IDataCollectorSet.Start, base.idatacollectorset_start, pla.idatacollectorset_start, pla/IDataCollectorSet::Start
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorSet.Start
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataCollectorSet::Start method


## -description


Manually starts the data collector set.


## -parameters




### -param Synchronous [in]

Data collection runs in a separate process. This value determines when the method returns. 

Set to VARIANT_TRUE to have the method return after the data collection process starts or fails to start. The return value indicates whether the set successfully started or failed to start.

Set to VARIANT_FALSE to return after the set is queued to run. The return value indicates whether the set was successfully queued. For more information, see Remarks.


## -returns



Returns <b>S_OK</b> if successful. The following table shows possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The set must be persisted (see the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> method) prior to starting collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the path specified. This error occurs when the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">RootPath</a> property specifies a directory that does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The subdirectory or log file already exists. Try using a format to uniquely identify the file.

</td>
</tr>
</table>
 




## -remarks



To determine the status of the collection, access the <a href="https://msdn.microsoft.com/d957d34d-5455-486a-bd54-28afd7e6f979">IDataCollectorSet::Status</a> property.

When the collection process is complete, PLA runs the <a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">data manager</a>, if enabled.

To automatically start data collection on a schedule, see <a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">IDataCollectorSet::Schedules</a>.

If you start the set asynchronously, an event is written to the Microsoft-Windows-Diagnosis-PLA/Operational event log to indicate whether the collection process started (event 1003) or failed (event 1004).




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">IDataCollectorSet::Schedules</a>



<a href="https://msdn.microsoft.com/b869ea8e-4fc8-4974-9e1c-1d2c480c3b0e">IDataCollectorSet::Stop</a>
 

 

