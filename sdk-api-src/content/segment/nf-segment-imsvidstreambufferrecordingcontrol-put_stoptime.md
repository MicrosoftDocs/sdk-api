---
UID: NF:segment.IMSVidStreamBufferRecordingControl.put_StopTime
title: IMSVidStreamBufferRecordingControl::put_StopTime (segment.h)
description: The put_StopTime method sets the stop time for the recording.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","put_StopTime method","IMSVidStreamBufferRecordingControl.put_StopTime","IMSVidStreamBufferRecordingControl::put_StopTime","IMSVidStreamBufferRecordingControlput_StopTime","mstv.imsvidstreambufferrecordingcontrol_put_stoptime","put_StopTime","put_StopTime method [Microsoft TV Technologies]","put_StopTime method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","segment/IMSVidStreamBufferRecordingControl::put_StopTime"]
old-location: mstv\imsvidstreambufferrecordingcontrol_put_stoptime.htm
tech.root: mstv
ms.assetid: 5ff338e8-4b91-4947-9ec6-fe35a3fcad3f
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],put_StopTime method, IMSVidStreamBufferRecordingControl.put_StopTime, IMSVidStreamBufferRecordingControl::put_StopTime, IMSVidStreamBufferRecordingControlput_StopTime, mstv.imsvidstreambufferrecordingcontrol_put_stoptime, put_StopTime, put_StopTime method [Microsoft TV Technologies], put_StopTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, segment/IMSVidStreamBufferRecordingControl::put_StopTime
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
 - IMSVidStreamBufferRecordingControl::put_StopTime
 - segment/IMSVidStreamBufferRecordingControl::put_StopTime
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
 - IMSVidStreamBufferRecordingControl.put_StopTime
---

# IMSVidStreamBufferRecordingControl::put_StopTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_StopTime</b> method sets the stop time for the recording.

## -parameters

### -param rtStop [in]

Specifies the stop time, in hundredths of seconds.

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