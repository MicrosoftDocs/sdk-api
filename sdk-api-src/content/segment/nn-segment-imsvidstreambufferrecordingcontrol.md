---
UID: NN:segment.IMSVidStreamBufferRecordingControl
title: IMSVidStreamBufferRecordingControl
author: windows-driver-content
description: The IMSVidStreamBufferRecordingControl interface enables an application to manage a stream buffer recording object through the Video Control.
old-location: mstv\imsvidstreambufferrecordingcontrol.htm
old-project: mstv
ms.assetid: a61414dc-a9a0-4c65-8f5a-eaabc79783e3
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferRecordingControl, IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies], IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies], described, IMSVidStreamBufferRecordingControlInterface, mstv.imsvidstreambufferrecordingcontrol, segment/IMSVidStreamBufferRecordingControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferRecordingControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferRecordingControl interface


## -description



The <b>IMSVidStreamBufferRecordingControl</b> interface enables an application to manage a stream buffer recording object through the Video Control. To obtain this interface, call one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/9fecdf37-0ad2-499b-8604-5e60bb0aa6e2">IMSVidStreamBufferSink::get_ContentRecorder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81315825-165a-48ef-be5e-fdeba67765f6">IMSVidStreamBufferSink::get_ReferenceRecorder</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferRecordingControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMSVidStreamBufferRecordingControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/259d0ca0-0566-443c-aa73-a28c304b9d1d">get_RecordingAttribute</a>
</td>
<td align="left" width="63%">
Retrieves the recording object that is controlled by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99abd883-5fec-4ac4-a167-aa2d4c3bf470">get_RecordingStarted</a>
</td>
<td align="left" width="63%">
Queries whether the recording has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894bed11-7bb6-49b9-8036-c32536949dbd">get_RecordingStopped</a>
</td>
<td align="left" width="63%">
Queries whether the recording has stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23f63c44-4970-42b2-a19a-0a28e7fb5dea">get_RecordingType</a>
</td>
<td align="left" width="63%">
Retrieves the type of recording, either content recording or reference recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3efe3cd3-cd26-4a91-b305-6e8677a0cd88">get_StartTime</a>
</td>
<td align="left" width="63%">
Retrieves the start time of the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17abe9d3-1a84-4dcf-bc61-d9eafe7418f7">get_StopTime</a>
</td>
<td align="left" width="63%">
Retrieves the stop time of the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/923fecbb-00f4-445f-a5cb-ef898580396e">put_StartTime</a>
</td>
<td align="left" width="63%">
Sets the start time for the recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ff338e8-4b91-4947-9ec6-fe35a3fcad3f">put_StopTime</a>
</td>
<td align="left" width="63%">
Sets the stop time for the recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferRecordingControl)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

