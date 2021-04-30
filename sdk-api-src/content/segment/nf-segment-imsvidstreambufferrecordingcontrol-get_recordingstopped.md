---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingStopped
title: IMSVidStreamBufferRecordingControl::get_RecordingStopped (segment.h)
description: The get_RecordingStopped method queries whether the recording has stopped.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","get_RecordingStopped method","IMSVidStreamBufferRecordingControl.get_RecordingStopped","IMSVidStreamBufferRecordingControl::get_RecordingStopped","IMSVidStreamBufferRecordingControlget_RecordingStopped","get_RecordingStopped","get_RecordingStopped method [Microsoft TV Technologies]","get_RecordingStopped method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","mstv.imsvidstreambufferrecordingcontrol_get_recordingstopped","segment/IMSVidStreamBufferRecordingControl::get_RecordingStopped"]
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingstopped.htm
tech.root: mstv
ms.assetid: 894bed11-7bb6-49b9-8036-c32536949dbd
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingStopped method, IMSVidStreamBufferRecordingControl.get_RecordingStopped, IMSVidStreamBufferRecordingControl::get_RecordingStopped, IMSVidStreamBufferRecordingControlget_RecordingStopped, get_RecordingStopped, get_RecordingStopped method [Microsoft TV Technologies], get_RecordingStopped method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingstopped, segment/IMSVidStreamBufferRecordingControl::get_RecordingStopped
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
 - IMSVidStreamBufferRecordingControl::get_RecordingStopped
 - segment/IMSVidStreamBufferRecordingControl::get_RecordingStopped
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
 - IMSVidStreamBufferRecordingControl.get_RecordingStopped
---

# IMSVidStreamBufferRecordingControl::get_RecordingStopped


## -description

The <b>get_RecordingStopped</b> method queries whether the recording has stopped.

## -parameters

### -param phResult [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The recording has not stopped.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The recording has stopped.</td>
</tr>
</table>

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