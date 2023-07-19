---
UID: NF:segment.IMSVidStreamBufferRecordingControl.put_StartTime
title: IMSVidStreamBufferRecordingControl::put_StartTime (segment.h)
description: The put_StartTime method sets the start time for the recording.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","put_StartTime method","IMSVidStreamBufferRecordingControl.put_StartTime","IMSVidStreamBufferRecordingControl::put_StartTime","IMSVidStreamBufferRecordingControlput_StartTime","mstv.imsvidstreambufferrecordingcontrol_put_starttime","put_StartTime","put_StartTime method [Microsoft TV Technologies]","put_StartTime method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","segment/IMSVidStreamBufferRecordingControl::put_StartTime"]
old-location: mstv\imsvidstreambufferrecordingcontrol_put_starttime.htm
tech.root: mstv
ms.assetid: 923fecbb-00f4-445f-a5cb-ef898580396e
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],put_StartTime method, IMSVidStreamBufferRecordingControl.put_StartTime, IMSVidStreamBufferRecordingControl::put_StartTime, IMSVidStreamBufferRecordingControlput_StartTime, mstv.imsvidstreambufferrecordingcontrol_put_starttime, put_StartTime, put_StartTime method [Microsoft TV Technologies], put_StartTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, segment/IMSVidStreamBufferRecordingControl::put_StartTime
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
 - IMSVidStreamBufferRecordingControl::put_StartTime
 - segment/IMSVidStreamBufferRecordingControl::put_StartTime
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
 - IMSVidStreamBufferRecordingControl.put_StartTime
---

# IMSVidStreamBufferRecordingControl::put_StartTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_StartTime</b> method sets the start time for the recording.

## -parameters

### -param rtStart [in]

Specifies the start time, in hundredths of seconds.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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