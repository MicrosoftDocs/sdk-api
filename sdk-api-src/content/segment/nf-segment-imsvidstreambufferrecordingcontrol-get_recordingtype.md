---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingType
title: IMSVidStreamBufferRecordingControl::get_RecordingType
author: windows-sdk-content
description: The get_RecordingType method retrieves the type of recording, either content recording or reference recording.
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingtype.htm
tech.root: MSTV
ms.assetid: 23f63c44-4970-42b2-a19a-0a28e7fb5dea
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingType method, IMSVidStreamBufferRecordingControl.get_RecordingType, IMSVidStreamBufferRecordingControl::get_RecordingType, IMSVidStreamBufferRecordingControlget_RecordingType, get_RecordingType, get_RecordingType method [Microsoft TV Technologies], get_RecordingType method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingtype, segment/IMSVidStreamBufferRecordingControl::get_RecordingType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/1aee15a3-5bc8-401b-9b37-b9351fd7c91f">Creating Stream Buffer Recordings</a>



<a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl Interface</a>
 

 

