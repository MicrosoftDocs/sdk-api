---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_StopTime
title: IMSVidStreamBufferRecordingControl::get_StopTime (segment.h)
description: The get_StopTime method retrieves the stop time of the recording.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","get_StopTime method","IMSVidStreamBufferRecordingControl.get_StopTime","IMSVidStreamBufferRecordingControl::get_StopTime","IMSVidStreamBufferRecordingControlget_StopTime","get_StopTime","get_StopTime method [Microsoft TV Technologies]","get_StopTime method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","mstv.imsvidstreambufferrecordingcontrol_get_stoptime","segment/IMSVidStreamBufferRecordingControl::get_StopTime"]
old-location: mstv\imsvidstreambufferrecordingcontrol_get_stoptime.htm
tech.root: mstv
ms.assetid: 17abe9d3-1a84-4dcf-bc61-d9eafe7418f7
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_StopTime method, IMSVidStreamBufferRecordingControl.get_StopTime, IMSVidStreamBufferRecordingControl::get_StopTime, IMSVidStreamBufferRecordingControlget_StopTime, get_StopTime, get_StopTime method [Microsoft TV Technologies], get_StopTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_stoptime, segment/IMSVidStreamBufferRecordingControl::get_StopTime
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidStreamBufferRecordingControl::get_StopTime
 - segment/IMSVidStreamBufferRecordingControl::get_StopTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferRecordingControl.get_StopTime
---

# IMSVidStreamBufferRecordingControl::get_StopTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_StopTime</b> method retrieves the stop time of the recording.

## -parameters

### -param rtStop [out]

Pointer to a variable that receives the stop time, in hundredths of seconds.

## -returns

The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl Interface</a>