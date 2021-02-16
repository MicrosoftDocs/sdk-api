---
UID: NF:pla.IDataCollectorSet.Stop
title: IDataCollectorSet::Stop (pla.h)
description: Manually stops the data collector set.
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Stop method","IDataCollectorSet.Stop","IDataCollectorSet::Stop","Stop","Stop method [PLA]","Stop method [PLA]","IDataCollectorSet interface","base.idatacollectorset_stop","pla.idatacollectorset_stop","pla/IDataCollectorSet::Stop"]
old-location: pla\idatacollectorset_stop.htm
tech.root: PLA
ms.assetid: b869ea8e-4fc8-4974-9e1c-1d2c480c3b0e
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Stop method, IDataCollectorSet.Stop, IDataCollectorSet::Stop, Stop, Stop method [PLA], Stop method [PLA],IDataCollectorSet interface, base.idatacollectorset_stop, pla.idatacollectorset_stop, pla/IDataCollectorSet::Stop
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
 - IDataCollectorSet::Stop
 - pla/IDataCollectorSet::Stop
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
 - IDataCollectorSet.Stop
---

# IDataCollectorSet::Stop


## -description

Manually stops the data collector set.

## -parameters

### -param Synchronous [in]

Data collection runs in a separate process. This value determines when the method returns. 

Set to VARIANT_TRUE to have the method return after the data collector set is stopped or fails to stop. The return value indicates whether the set successfully stopped or failed to stop.

Set to VARIANT_FALSE to return after the method sends a request to the set to stop. The return value indicates whether the request was successfully sent to the set. An event is written to the event log if the set fails to stop.

## -returns

Returns S_OK if successful. The following table shows a possible error value.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLA_E_DCS_NOT_RUNNING</b></dt>
<dt>0x80300104</dt>
</dl>
</td>
<td width="60%">
The data collector set is not running.

</td>
</tr>
</table>

## -remarks

This method saves the data already collected when the set is stopped.

Note that if the <i>Synchronous</i> parameter is VARIANT_TRUE, the method will not return until data management and tasks that run after collection are complete.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">IDataCollectorSet::Start</a>