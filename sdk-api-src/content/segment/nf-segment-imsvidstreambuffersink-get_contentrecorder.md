---
UID: NF:segment.IMSVidStreamBufferSink.get_ContentRecorder
title: IMSVidStreamBufferSink::get_ContentRecorder (segment.h)
description: The get_ContentRecorder method creates a new content recording object.
helpviewer_keywords: ["IMSVidStreamBufferSink interface [Microsoft TV Technologies]","get_ContentRecorder method","IMSVidStreamBufferSink.get_ContentRecorder","IMSVidStreamBufferSink::get_ContentRecorder","IMSVidStreamBufferSinkget_ContentRecorder","get_ContentRecorder","get_ContentRecorder method [Microsoft TV Technologies]","get_ContentRecorder method [Microsoft TV Technologies]","IMSVidStreamBufferSink interface","mstv.imsvidstreambuffersink_get_contentrecorder","segment/IMSVidStreamBufferSink::get_ContentRecorder"]
old-location: mstv\imsvidstreambuffersink_get_contentrecorder.htm
tech.root: mstv
ms.assetid: 9fecdf37-0ad2-499b-8604-5e60bb0aa6e2
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_ContentRecorder method, IMSVidStreamBufferSink.get_ContentRecorder, IMSVidStreamBufferSink::get_ContentRecorder, IMSVidStreamBufferSinkget_ContentRecorder, get_ContentRecorder, get_ContentRecorder method [Microsoft TV Technologies], get_ContentRecorder method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_contentrecorder, segment/IMSVidStreamBufferSink::get_ContentRecorder
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
 - IMSVidStreamBufferSink::get_ContentRecorder
 - segment/IMSVidStreamBufferSink::get_ContentRecorder
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
 - IMSVidStreamBufferSink.get_ContentRecorder
---

# IMSVidStreamBufferSink::get_ContentRecorder


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ContentRecorder</b> method creates a new content recording object.

## -parameters

### -param pszFilename [in]

Specifies the name of the file to hold the recording.

### -param pRecordingIUnknown [out]

Receives a pointer to the recording object's <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl</a> interface.

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

The caller must release the returned <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersink">IMSVidStreamBufferSink Interface</a>