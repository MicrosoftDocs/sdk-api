---
UID: NF:sbe.IStreamBufferRecordControl.Start
title: IStreamBufferRecordControl::Start (sbe.h)
description: The Start method starts the recording.
helpviewer_keywords: ["IStreamBufferRecordControl interface [Microsoft TV Technologies]","Start method","IStreamBufferRecordControl.Start","IStreamBufferRecordControl::Start","IStreamBufferRecordControlStart","Start","Start method [Microsoft TV Technologies]","Start method [Microsoft TV Technologies]","IStreamBufferRecordControl interface","mstv.istreambufferrecordcontrol_start","sbe/IStreamBufferRecordControl::Start"]
old-location: mstv\istreambufferrecordcontrol_start.htm
tech.root: mstv
ms.assetid: e72ec34e-d3e3-4f5f-9336-d55135dc1e47
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordControl interface [Microsoft TV Technologies],Start method, IStreamBufferRecordControl.Start, IStreamBufferRecordControl::Start, IStreamBufferRecordControlStart, Start, Start method [Microsoft TV Technologies], Start method [Microsoft TV Technologies],IStreamBufferRecordControl interface, mstv.istreambufferrecordcontrol_start, sbe/IStreamBufferRecordControl::Start
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferRecordControl::Start
 - sbe/IStreamBufferRecordControl::Start
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecordControl.Start
---

# IStreamBufferRecordControl::Start


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Start</b> method starts the recording.

## -parameters

### -param prtStart [in, out]

Pointer to a variable that contains the start time. The time is relative to the current stream time, in 100-nanosecond units. The value zero represents now; negative values are in the past; and positive values are in the future.

For content recordings, the time must be a value between 0 and 5 seconds (50000000), inclusive. Negative times are not valid.

For reference recordings, negative times are valid if they fall within existing content. If the time given in <i>prtStart</i> is earlier than the earliest valid content, the actual start time of the content is used instead. This value is returned in <i>prtStart</i> when the method returns.

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
Invalid time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The start time must be less than or equal to the stop time.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordcontrol">IStreamBufferRecordControl Interface</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-stop">IStreamBufferRecordControl::Stop</a>