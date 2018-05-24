---
UID: NF:segment.IMSVidStreamBufferRecordingControl.put_StopTime
title: IMSVidStreamBufferRecordingControl::put_StopTime
author: windows-driver-content
description: The put_StopTime method sets the stop time for the recording.
old-location: mstv\imsvidstreambufferrecordingcontrol_put_stoptime.htm
old-project: mstv
ms.assetid: 5ff338e8-4b91-4947-9ec6-fe35a3fcad3f
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],put_StopTime method, IMSVidStreamBufferRecordingControl.put_StopTime, IMSVidStreamBufferRecordingControl::put_StopTime, IMSVidStreamBufferRecordingControlput_StopTime, mstv.imsvidstreambufferrecordingcontrol_put_stoptime, put_StopTime, put_StopTime method [Microsoft TV Technologies], put_StopTime method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, segment/IMSVidStreamBufferRecordingControl::put_StopTime
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
-	IMSVidStreamBufferRecordingControl.put_StopTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferRecordingControl::put_StopTime


## -description


The <b>put_StopTime</b> method sets the stop time for the recording.


## -parameters




### -param rtStop






#### - Stop [in]

Specifies the stop time, in hundredths of seconds.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
 

 

