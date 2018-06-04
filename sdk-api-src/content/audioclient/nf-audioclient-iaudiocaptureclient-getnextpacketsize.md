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

# IAudioCaptureClient::GetNextPacketSize


## -description



The <b>GetNextPacketSize</b> method retrieves the number of frames in the next data packet in the capture endpoint buffer.




## -parameters




### -param pNumFramesInNextPacket [out]

Pointer to a <b>UINT32</b> variable into which the method writes the frame count (the number of audio frames in the next capture packet).


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pNumFramesInNextPacket</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Use this method only with shared-mode streams. It does not work with exclusive-mode streams.

Before calling the <a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a> method to retrieve the next data packet, the client can call <b>GetNextPacketSize</b> to retrieve the number of audio frames in the next packet. The count reported by <b>GetNextPacketSize</b> matches the count retrieved in the <b>GetBuffer</b> call (through the <i>pNumFramesToRead</i> output parameter) that follows the <b>GetNextPacketSize</b> call.

A packet always consists of an integral number of audio frames.

<b>GetNextPacketSize</b> must be called in the same thread as the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> and <a href="https://msdn.microsoft.com/38e1ea6c-d07d-4075-b6f2-d563c4bce007">IAudioCaptureClient::ReleaseBuffer</a> method calls that get and release the packets in the capture endpoint buffer.

For a code example that uses the <b>GetNextPacketSize</b> method, see <a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0fa6841-56bf-421e-9949-c6a037cf9fd4">IAudioCaptureClient Interface</a>



<a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a>



<a href="https://msdn.microsoft.com/38e1ea6c-d07d-4075-b6f2-d563c4bce007">IAudioCaptureClient::ReleaseBuffer</a>



<a href="https://msdn.microsoft.com/2a2c9ddf-f668-41ff-85f0-34de593c0fe2">IAudioClient::GetCurrentPadding</a>
 

 

