---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingStarted
title: IMSVidStreamBufferRecordingControl::get_RecordingStarted method
author: windows-driver-content
description: The get_RecordingStarted method queries whether the recording has started.
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingstarted.htm
old-project: mstv
ms.assetid: 99abd883-5fec-4ac4-a167-aa2d4c3bf470
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferRecordingControl, IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies], get_RecordingStarted method, IMSVidStreamBufferRecordingControl::get_RecordingStarted, IMSVidStreamBufferRecordingControlget_RecordingStarted, get_RecordingStarted method [Microsoft TV Technologies], get_RecordingStarted method [Microsoft TV Technologies], IMSVidStreamBufferRecordingControl interface, get_RecordingStarted,IMSVidStreamBufferRecordingControl.get_RecordingStarted, mstv.imsvidstreambufferrecordingcontrol_get_recordingstarted, segment/IMSVidStreamBufferRecordingControl::get_RecordingStarted
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferRecordingControl.get_RecordingStarted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferRecordingControl::get_RecordingStarted method


## -description


The <b>get_RecordingStarted</b> method queries whether the recording has started.


## -parameters




### -param phResult [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The recording has not started.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The recording has started.</td>
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




<a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl Interface</a>
 

 

