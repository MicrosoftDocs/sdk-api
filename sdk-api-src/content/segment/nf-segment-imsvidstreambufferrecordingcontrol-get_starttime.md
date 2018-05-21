---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_StartTime
title: IMSVidStreamBufferRecordingControl::get_StartTime
author: windows-driver-content
description: The get_StartTime method retrieves the start time of the recording.
old-location: mstv\imsvidstreambufferrecordingcontrol_get_starttime.htm
old-project: mstv
ms.assetid: 3efe3cd3-cd26-4a91-b305-6e8677a0cd88
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_StartTime method, IMSVidStreamBufferRecordingControl.get_StartTime, IMSVidStreamBufferRecordingControl::get_StartTime, IMSVidStreamBufferRecordingControlget_StartTime, get_StartTime, get_StartTime method [Microsoft TV Technologies], get_StartTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_starttime, segment/IMSVidStreamBufferRecordingControl::get_StartTime
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
-	IMSVidStreamBufferRecordingControl.get_StartTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferRecordingControl::get_StartTime


## -description


The <b>get_StartTime</b> method retrieves the start time of the recording.


## -parameters




### -param rtStart






#### - pStart [out]

Pointer to a variable that receives the start time, in hundredths of seconds.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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
 

 

