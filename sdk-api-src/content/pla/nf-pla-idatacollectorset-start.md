---
UID: NF:pla.IDataCollectorSet.Start
title: IDataCollectorSet::Start (pla.h)
description: Manually starts the data collector set.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Start method","IDataCollectorSet.Start","IDataCollectorSet::Start","Start","Start method [PLA]","Start method [PLA]","IDataCollectorSet interface","base.idatacollectorset_start","pla.idatacollectorset_start","pla/IDataCollectorSet::Start"]
old-location: pla\idatacollectorset_start.htm
tech.root: PLA
ms.assetid: 63f0c7b7-0dc6-4491-a2f5-eaae9d22da61
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Start method, IDataCollectorSet.Start, IDataCollectorSet::Start, Start, Start method [PLA], Start method [PLA],IDataCollectorSet interface, base.idatacollectorset_start, pla.idatacollectorset_start, pla/IDataCollectorSet::Start
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
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSet::Start
 - pla/IDataCollectorSet::Start
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Start
---

# IDataCollectorSet::Start


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
The set must be persisted (see the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">Commit</a> method) prior to starting collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the path specified. This error occurs when the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">RootPath</a> property specifies a directory that does not exist.

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

To determine the status of the collection, access the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_status">IDataCollectorSet::Status</a> property.

When the collection process is complete, PLA runs the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">data manager</a>, if enabled.

To automatically start data collection on a schedule, see <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a>.

If you start the set asynchronously, an event is written to the Microsoft-Windows-Diagnosis-PLA/Operational event log to indicate whether the collection process started (event 1003) or failed (event 1004).

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-stop">IDataCollectorSet::Stop</a>