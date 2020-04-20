---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingType
title: IMSVidStreamBufferRecordingControl::get_RecordingType (segment.h)
description: The get_RecordingType method retrieves the type of recording, either content recording or reference recording.helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","get_RecordingType method","IMSVidStreamBufferRecordingControl.get_RecordingType","IMSVidStreamBufferRecordingControl::get_RecordingType","IMSVidStreamBufferRecordingControlget_RecordingType","get_RecordingType","get_RecordingType method [Microsoft TV Technologies]","get_RecordingType method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","mstv.imsvidstreambufferrecordingcontrol_get_recordingtype","segment/IMSVidStreamBufferRecordingControl::get_RecordingType"]
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingtype.htm
tech.root: mstv
ms.assetid: 23f63c44-4970-42b2-a19a-0a28e7fb5dea
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingType method, IMSVidStreamBufferRecordingControl.get_RecordingType, IMSVidStreamBufferRecordingControl::get_RecordingType, IMSVidStreamBufferRecordingControlget_RecordingType, get_RecordingType, get_RecordingType method [Microsoft TV Technologies], get_RecordingType method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingtype, segment/IMSVidStreamBufferRecordingControl::get_RecordingType
f1_keywords:
- segment/IMSVidStreamBufferRecordingControl.get_RecordingType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidStreamBufferRecordingControl.get_RecordingType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferRecordingControl::get_RecordingType


## -description


The <b>get_RecordingType</b> method retrieves the type of recording, either content recording or reference recording.


## -parameters




### -param dwType [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>CONTENT</td>
<td>Content recording</td>
</tr>
<tr>
<td>REFERENCE</td>
<td>Reference recording</td>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/creating-stream-buffer-recordings">Creating Stream Buffer Recordings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl Interface</a>
 

 

