---
UID: NF:sbe.IStreamBufferRecordControl.Start
title: IStreamBufferRecordControl::Start
author: windows-driver-content
description: The Start method starts the recording.
old-location: mstv\istreambufferrecordcontrol_start.htm
old-project: mstv
ms.assetid: e72ec34e-d3e3-4f5f-9336-d55135dc1e47
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IStreamBufferRecordControl interface [Microsoft TV Technologies],Start method, IStreamBufferRecordControl.Start, IStreamBufferRecordControl::Start, IStreamBufferRecordControlStart, Start, Start method [Microsoft TV Technologies], Start method [Microsoft TV Technologies],IStreamBufferRecordControl interface, mstv.istreambufferrecordcontrol_start, sbe/IStreamBufferRecordControl::Start
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferRecordControl.Start
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStreamBufferRecordControl::Start


## -description


The <b>Start</b> method starts the recording.


## -parameters




### -param prtStart [in, out]

Pointer to a variable that contains the start time. The time is relative to the current stream time, in 100-nanosecond units. The value zero represents now; negative values are in the past; and positive values are in the future.

For content recordings, the time must be a value between 0 and 5 seconds (50000000), inclusive. Negative times are not valid.

For reference recordings, negative times are valid if they fall within existing content. If the time given in <i>prtStart</i> is earlier than the earliest valid content, the actual start time of the content is used instead. This value is returned in <i>prtStart</i> when the method returns.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
Invalid time.

</td>
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
 




## -remarks



The start time must be less than or equal to the stop time.




## -see-also




<a href="https://msdn.microsoft.com/f196638e-ccbb-4768-96c1-8e1d00361831">IStreamBufferRecordControl Interface</a>



<a href="https://msdn.microsoft.com/1b6a3ac4-076a-4fca-909c-6063637248a8">IStreamBufferRecordControl::Stop</a>
 

 

