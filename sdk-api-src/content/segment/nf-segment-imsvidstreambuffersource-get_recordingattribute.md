---
UID: NF:segment.IMSVidStreamBufferSource.get_RecordingAttribute
title: IMSVidStreamBufferSource::get_RecordingAttribute (segment.h)
description: The get_RecordingAttribute method retrieves the Stream Buffer Source filter that this object manages.
helpviewer_keywords: ["IMSVidStreamBufferSource interface [Microsoft TV Technologies]","get_RecordingAttribute method","IMSVidStreamBufferSource.get_RecordingAttribute","IMSVidStreamBufferSource::get_RecordingAttribute","IMSVidStreamBufferSourceget_RecordingAttribute","get_RecordingAttribute","get_RecordingAttribute method [Microsoft TV Technologies]","get_RecordingAttribute method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","mstv.imsvidstreambuffersource_get_recordingattribute","segment/IMSVidStreamBufferSource::get_RecordingAttribute"]
old-location: mstv\imsvidstreambuffersource_get_recordingattribute.htm
tech.root: mstv
ms.assetid: 9e7020c8-778d-4a24-ae29-3e66d4ac165a
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],get_RecordingAttribute method, IMSVidStreamBufferSource.get_RecordingAttribute, IMSVidStreamBufferSource::get_RecordingAttribute, IMSVidStreamBufferSourceget_RecordingAttribute, get_RecordingAttribute, get_RecordingAttribute method [Microsoft TV Technologies], get_RecordingAttribute method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_get_recordingattribute, segment/IMSVidStreamBufferSource::get_RecordingAttribute
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
 - IMSVidStreamBufferSource::get_RecordingAttribute
 - segment/IMSVidStreamBufferSource::get_RecordingAttribute
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
 - IMSVidStreamBufferSource.get_RecordingAttribute
---

# IMSVidStreamBufferSource::get_RecordingAttribute


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_RecordingAttribute</b> method retrieves the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter that this object manages.

## -parameters

### -param pRecordingAttribute [out]

Receives a pointer to the filter's <b>IUnknown</b> interface.

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

The caller must release the returned <b>IUnknown</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource Interface</a>