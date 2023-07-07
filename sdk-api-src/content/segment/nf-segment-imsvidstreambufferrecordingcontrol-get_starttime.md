---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_StartTime
title: IMSVidStreamBufferRecordingControl::get_StartTime (segment.h)
description: The get_StartTime method retrieves the start time of the recording.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","get_StartTime method","IMSVidStreamBufferRecordingControl.get_StartTime","IMSVidStreamBufferRecordingControl::get_StartTime","IMSVidStreamBufferRecordingControlget_StartTime","get_StartTime","get_StartTime method [Microsoft TV Technologies]","get_StartTime method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","mstv.imsvidstreambufferrecordingcontrol_get_starttime","segment/IMSVidStreamBufferRecordingControl::get_StartTime"]
old-location: mstv\imsvidstreambufferrecordingcontrol_get_starttime.htm
tech.root: mstv
ms.assetid: 3efe3cd3-cd26-4a91-b305-6e8677a0cd88
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_StartTime method, IMSVidStreamBufferRecordingControl.get_StartTime, IMSVidStreamBufferRecordingControl::get_StartTime, IMSVidStreamBufferRecordingControlget_StartTime, get_StartTime, get_StartTime method [Microsoft TV Technologies], get_StartTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_starttime, segment/IMSVidStreamBufferRecordingControl::get_StartTime
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
 - IMSVidStreamBufferRecordingControl::get_StartTime
 - segment/IMSVidStreamBufferRecordingControl::get_StartTime
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
 - IMSVidStreamBufferRecordingControl.get_StartTime
---

# IMSVidStreamBufferRecordingControl::get_StartTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_StartTime</b> method retrieves the start time of the recording.

## -parameters

### -param rtStart [out]

Pointer to a variable that receives the start time, in hundredths of seconds.

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