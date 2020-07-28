---
UID: NN:segment.IMSVidStreamBufferRecordingControl
title: IMSVidStreamBufferRecordingControl (segment.h)
description: The IMSVidStreamBufferRecordingControl interface enables an application to manage a stream buffer recording object through the Video Control.
helpviewer_keywords: ["IMSVidStreamBufferRecordingControl","IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies]","described","IMSVidStreamBufferRecordingControlInterface","mstv.imsvidstreambufferrecordingcontrol","segment/IMSVidStreamBufferRecordingControl"]
old-location: mstv\imsvidstreambufferrecordingcontrol.htm
tech.root: mstv
ms.assetid: a61414dc-a9a0-4c65-8f5a-eaabc79783e3
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferRecordingControl, IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies], IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],described, IMSVidStreamBufferRecordingControlInterface, mstv.imsvidstreambufferrecordingcontrol, segment/IMSVidStreamBufferRecordingControl
f1_keywords:
- segment/IMSVidStreamBufferRecordingControl
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
- IMSVidStreamBufferRecordingControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferRecordingControl interface


## -description



The <b>IMSVidStreamBufferRecordingControl</b> interface enables an application to manage a stream buffer recording object through the Video Control. To obtain this interface, call one of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_contentrecorder">IMSVidStreamBufferSink::get_ContentRecorder</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersink-get_referencerecorder">IMSVidStreamBufferSink::get_ReferenceRecorder</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferRecordingControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidStreamBufferRecordingControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferRecordingControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_recordingattribute">get_RecordingAttribute</a>
</td>
<td align="left" width="63%">
Retrieves the recording object that is controlled by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_recordingstarted">get_RecordingStarted</a>
</td>
<td align="left" width="63%">
Queries whether the recording has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_recordingstopped">get_RecordingStopped</a>
</td>
<td align="left" width="63%">
Queries whether the recording has stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_recordingtype">get_RecordingType</a>
</td>
<td align="left" width="63%">
Retrieves the type of recording, either content recording or reference recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_starttime">get_StartTime</a>
</td>
<td align="left" width="63%">
Retrieves the start time of the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-get_stoptime">get_StopTime</a>
</td>
<td align="left" width="63%">
Retrieves the stop time of the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-put_starttime">put_StartTime</a>
</td>
<td align="left" width="63%">
Sets the start time for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferrecordingcontrol-put_stoptime">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets the stop time for the recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferRecordingControl)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

