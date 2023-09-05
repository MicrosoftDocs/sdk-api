---
UID: NF:sbe.IStreamBufferRecordControl.Stop
title: IStreamBufferRecordControl::Stop (sbe.h)
description: The Stop method stops the recording and closes the file.
helpviewer_keywords: ["IStreamBufferRecordControl interface [Microsoft TV Technologies]","Stop method","IStreamBufferRecordControl.Stop","IStreamBufferRecordControl::Stop","IStreamBufferRecordControlStop","Stop","Stop method [Microsoft TV Technologies]","Stop method [Microsoft TV Technologies]","IStreamBufferRecordControl interface","mstv.istreambufferrecordcontrol_stop","sbe/IStreamBufferRecordControl::Stop"]
old-location: mstv\istreambufferrecordcontrol_stop.htm
tech.root: mstv
ms.assetid: 1b6a3ac4-076a-4fca-909c-6063637248a8
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordControl interface [Microsoft TV Technologies],Stop method, IStreamBufferRecordControl.Stop, IStreamBufferRecordControl::Stop, IStreamBufferRecordControlStop, Stop, Stop method [Microsoft TV Technologies], Stop method [Microsoft TV Technologies],IStreamBufferRecordControl interface, mstv.istreambufferrecordcontrol_stop, sbe/IStreamBufferRecordControl::Stop
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
 - IStreamBufferRecordControl::Stop
 - sbe/IStreamBufferRecordControl::Stop
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
 - IStreamBufferRecordControl.Stop
---

# IStreamBufferRecordControl::Stop


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Stop</b> method stops the recording and closes the file.

## -parameters

### -param rtStop [in]

Specifies when the recording stops. The time is relative to the current stream time, in 100-nanosecond units. The value zero represents now; negative values are in the past; and positive values are in the future.

For content recordings, the valid range is from 0 to 5 seconds (50000000), inclusive. Negative times are not valid.

For reference recordings, a negative time is valid if it falls within valid recorded content.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

The stop time must be greater than or equal to the start time.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordcontrol">IStreamBufferRecordControl Interface</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">IStreamBufferRecordControl::Start</a>