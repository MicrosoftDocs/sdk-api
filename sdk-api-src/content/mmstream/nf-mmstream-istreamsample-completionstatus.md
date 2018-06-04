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

# IStreamSample::CompletionStatus


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the status of the current sample's latest asynchronous update. If the update isn't complete, you can force it to complete.




## -parameters




### -param dwFlags [in]

Value that specifies whether to forcibly complete the update. This value is a combination of one or more of the following flags.

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
<td>COMPSTAT_NOUPDATEOK (0x01)</td>
<td>Force the update to complete as soon as possible, even if the sample update isn't yet complete. If the sample is updating and you didn't set the COMPSTAT_WAIT flag, the method returns MS_S_PENDING. If the sample is waiting to be updated, this method removes it from the queue and returns MS_S_NOTUPDATED.</td>
</tr>
<tr>
<td>COMPSTAT_WAIT (0x02)</td>
<td>Wait until the sample finishes updating before returning from this method.</td>
</tr>
<tr>
<td>COMPSTAT_ABORT (0x04)</td>
<td>Forces the update to complete, even if it's currently updating. This leaves the sample data in an undefined state. Combine this value with the COMPSTAT_WAITFORCOMPLETION flag to ensure that the update canceled.</td>
</tr>
</table>
 


### -param dwMilliseconds [in]

If the <i>dwFlags</i> parameter is COMPSTAT_WAIT, this value is the number of milliseconds to wait for the update to complete. Specify INFINITE to indicate that you want to wait until the sample updates before this call returns.


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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The update aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_ENDOFSTREAM</b></dt>
</dl>
</td>
<td width="60%">
The sample wasn't updated because it reached the end of the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_NOUPDATE</b></dt>
</dl>
</td>
<td width="60%">
The update was forcibly completed; the sample was not updated by the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
An asynchronous update is pending.

</td>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample Interface</a>
 

 

