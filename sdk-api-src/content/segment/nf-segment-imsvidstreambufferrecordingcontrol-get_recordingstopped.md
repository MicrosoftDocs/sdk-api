---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingStopped
title: IMSVidStreamBufferRecordingControl::get_RecordingStopped
author: windows-sdk-content
description: The get_RecordingStopped method queries whether the recording has stopped.
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingstopped.htm
tech.root: MSTV
ms.assetid: 894bed11-7bb6-49b9-8036-c32536949dbd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingStopped method, IMSVidStreamBufferRecordingControl.get_RecordingStopped, IMSVidStreamBufferRecordingControl::get_RecordingStopped, IMSVidStreamBufferRecordingControlget_RecordingStopped, get_RecordingStopped, get_RecordingStopped method [Microsoft TV Technologies], get_RecordingStopped method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingstopped, segment/IMSVidStreamBufferRecordingControl::get_RecordingStopped
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
 - IMSVidStreamBufferRecordingControl.get_RecordingStopped
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidStreamBufferRecordingControl.get_RecordingStopped
: 
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




<a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl Interface</a>
 

 

