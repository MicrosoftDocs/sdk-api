---
UID: NF:amstream.IAMMediaTypeSample.GetTime
title: IAMMediaTypeSample::GetTime method
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. The GetTime method retrieves the stream times at which the sample should start and stop.
old-location: dshow\iammediatypesample_gettime.htm
old-project: DirectShow
ms.assetid: ffbbc857-ddcc-4625-b591-b95a256d40ba
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTime method [DirectShow], GetTime method [DirectShow], IAMMediaTypeSample interface, GetTime,IAMMediaTypeSample.GetTime, IAMMediaTypeSample, IAMMediaTypeSample interface [DirectShow], GetTime method, IAMMediaTypeSample::GetTime, IAMMediaTypeSampleGetTime, amstream/IAMMediaTypeSample::GetTime, dshow.iammediatypesample_gettime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IAMMediaTypeSample.GetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAMMediaTypeSample::GetTime method


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetTime</code> method retrieves the stream times at which the sample should start and stop.




## -parameters




### -param pTimeStart [out]

Pointer to a variable that receives the start time.


### -param pTimeEnd [out]

Pointer to a variable that receives the stop time. If the sample has no stop time, the value is set to the start time plus one.


## -returns



Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_SAMPLE_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The sample does not have any time stamps.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_NO_STOP_TIME</b></dt>
</dl>
</td>
<td width="60%">
The sample has a valid start time but no stop time.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

