---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IStreamBufferRecordControl::GetRecordingStatus


## -description


The <b>GetRecordingStatus</b> method retrieves the status of the recording.


## -parameters




### -param phResult




### -param pbStarted [out]

Pointer to a variable that receives a Boolean value, indicating whether the recording has started,

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
<th>
                  Value
                </th>
<th>
                  Description
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
 

 

