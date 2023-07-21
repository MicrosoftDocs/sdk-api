---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingAttribute
title: IMSVidStreamBufferRecordingControl::get_RecordingAttribute (segment.h)
description: The get_RecordingAttribute method retrieves the stream buffer Recording object that is controlled by this interface.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","get_RecordingAttribute method","IMSVidStreamBufferRecordingControl.get_RecordingAttribute","IMSVidStreamBufferRecordingControl::get_RecordingAttribute","IMSVidStreamBufferRecordingControlget_RecordingAttribute","get_RecordingAttribute","get_RecordingAttribute method [Microsoft TV Technologies]","get_RecordingAttribute method [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface","mstv.imsvidstreambufferrecordingcontrol_get_recordingattribute","segment/IMSVidStreamBufferRecordingControl::get_RecordingAttribute"]
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingattribute.htm
tech.root: mstv
ms.assetid: 259d0ca0-0566-443c-aa73-a28c304b9d1d
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingAttribute method, IMSVidStreamBufferRecordingControl.get_RecordingAttribute, IMSVidStreamBufferRecordingControl::get_RecordingAttribute, IMSVidStreamBufferRecordingControlget_RecordingAttribute, get_RecordingAttribute, get_RecordingAttribute method [Microsoft TV Technologies], get_RecordingAttribute method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingattribute, segment/IMSVidStreamBufferRecordingControl::get_RecordingAttribute
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
 - IMSVidStreamBufferRecordingControl::get_RecordingAttribute
 - segment/IMSVidStreamBufferRecordingControl::get_RecordingAttribute
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
 - IMSVidStreamBufferRecordingControl.get_RecordingAttribute
---

# IMSVidStreamBufferRecordingControl::get_RecordingAttribute


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_RecordingAttribute</b> method retrieves the stream buffer <a href="/previous-versions/windows/desktop/mstv/recording-object">Recording</a> object that is controlled by this interface.

## -parameters

### -param pRecordingAttribute [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/mstv/recording-object">Recording</a> object's <b>IUnknown</b> interface.

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

## -remarks

The caller must release the returned <b>IUnknown</b> pointer.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl Interface</a>