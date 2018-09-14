---
UID: NF:sbe.IStreamBufferRecordControl.GetRecordingStatus
title: IStreamBufferRecordControl::GetRecordingStatus
author: windows-sdk-content
description: The GetRecordingStatus method retrieves the status of the recording.
old-location: mstv\istreambufferrecordcontrol_getrecordingstatus.htm
tech.root: MSTV
ms.assetid: 313f2ad0-7401-4a36-a229-abfc67737324
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordingStatus, GetRecordingStatus method [Microsoft TV Technologies], GetRecordingStatus method [Microsoft TV Technologies],IStreamBufferRecordControl interface, IStreamBufferRecordControl interface [Microsoft TV Technologies],GetRecordingStatus method, IStreamBufferRecordControl.GetRecordingStatus, IStreamBufferRecordControl::GetRecordingStatus, IStreamBufferRecordControlGetRecordingStatus, mstv.istreambufferrecordcontrol_getrecordingstatus, sbe/IStreamBufferRecordControl::GetRecordingStatus
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecordControl.GetRecordingStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferRecordControl::GetRecordingStatus


## -description


The <b>GetRecordingStatus</b> method retrieves the status of the recording.


## -parameters




### -param phResult

TBD


### -param pbStarted [out]

Pointer to a variable that receives a Boolean value, indicating whether the recording has started,

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The recording has started.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The recording has not started.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.


### -param pbStopped [out]

Pointer to a variable that receives a Boolean value, indicating whether recording has been stopped.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The recording has stopped.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The recording has not stopped, or has not started yet.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.


#### - phLastResult [out]

Pointer to a variable that receives an <b>HRESULT</b> value. The <b>HRESULT</b> value indicates the current status of writing or closing the file. This parameter can be <b>NULL</b>.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method reports the status of the <b>Start</b> and <b>Stop</b> methods, which themselves are asynchronous.




## -see-also




<a href="https://msdn.microsoft.com/f196638e-ccbb-4768-96c1-8e1d00361831">IStreamBufferRecordControl Interface</a>
 

 

