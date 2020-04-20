---
UID: NF:segment.IMSVidStreamBufferSink.get_ReferenceRecorder
title: IMSVidStreamBufferSink::get_ReferenceRecorder (segment.h)
description: The get_ReferenceRecorder method creates a new reference recording object.helpviewer_keywords: ["IMSVidStreamBufferSink interface [Microsoft TV Technologies]","get_ReferenceRecorder method","IMSVidStreamBufferSink.get_ReferenceRecorder","IMSVidStreamBufferSink::get_ReferenceRecorder","IMSVidStreamBufferSinkget_ReferenceRecorder","get_ReferenceRecorder","get_ReferenceRecorder method [Microsoft TV Technologies]","get_ReferenceRecorder method [Microsoft TV Technologies]","IMSVidStreamBufferSink interface","mstv.imsvidstreambuffersink_get_referencerecorder","segment/IMSVidStreamBufferSink::get_ReferenceRecorder"]
old-location: mstv\imsvidstreambuffersink_get_referencerecorder.htm
tech.root: mstv
ms.assetid: 81315825-165a-48ef-be5e-fdeba67765f6
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_ReferenceRecorder method, IMSVidStreamBufferSink.get_ReferenceRecorder, IMSVidStreamBufferSink::get_ReferenceRecorder, IMSVidStreamBufferSinkget_ReferenceRecorder, get_ReferenceRecorder, get_ReferenceRecorder method [Microsoft TV Technologies], get_ReferenceRecorder method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_referencerecorder, segment/IMSVidStreamBufferSink::get_ReferenceRecorder
f1_keywords:
- segment/IMSVidStreamBufferSink.get_ReferenceRecorder
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
- IMSVidStreamBufferSink.get_ReferenceRecorder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSink::get_ReferenceRecorder


## -description


The <b>get_ReferenceRecorder</b> method creates a new reference recording object.


## -parameters




### -param pszFilename [in]

Specifies the name of the file to hold the recording.


### -param pRecordingIUnknown [out]

Receives a pointer to the recording object's <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl</a> interface.


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



The caller must release the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambufferrecordingcontrol">IMSVidStreamBufferRecordingControl</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidstreambuffersink">IMSVidStreamBufferSink Interface</a>
 

 

