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

# IAudioCaptureClient::ReleaseBuffer


## -description



The <b>ReleaseBuffer</b> method releases the buffer.




## -parameters




### -param NumFramesRead [in]

The number of audio frames that the client read from the capture buffer. This parameter must be either equal to the number of frames in the previously acquired data packet or 0.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>NumFramesRead</i> parameter is set to a value other than the data packet size or 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
This call was not preceded by a corresponding <a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



The client should call this method when it finishes reading a data packet that it obtained previously by calling the <a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a> method.

The data in the packet that the client obtained from a <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> call is guaranteed to remain valid until the client calls <b>ReleaseBuffer</b> to release the packet.

Between each <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> call and its corresponding <b>ReleaseBuffer</b> call, the client must either read the entire data packet or none of it. If the client reads the entire packet following the <b>GetBuffer</b> call, then it should call <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to the total number of frames in the data packet. In this case, the next call to <b>GetBuffer</b> will produce a new data packet. If the client reads none of the data from the packet following the call to <b>GetBuffer</b>, then it should call <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to 0. In this case, the next <b>GetBuffer</b> call will produce the same data packet as in the previous <b>GetBuffer</b> call.

If the client calls <b>ReleaseBuffer</b> with <i>NumFramesRead</i> set to any value other than the packet size or 0, then the call fails and returns error code AUDCLNT_E_INVALID_SIZE.

Clients should avoid excessive delays between the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> call that acquires a buffer and the <b>ReleaseBuffer</b> call that releases the buffer. The implementation of the audio engine assumes that the <b>GetBuffer</b> call and the corresponding <b>ReleaseBuffer</b> call occur within the same buffer-processing period. Clients that delay releasing a buffer for more than one period risk losing sample data.

For a code example that calls the <b>ReleaseBuffer</b> method, see <a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0fa6841-56bf-421e-9949-c6a037cf9fd4">IAudioCaptureClient Interface</a>



<a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a>
 

 

