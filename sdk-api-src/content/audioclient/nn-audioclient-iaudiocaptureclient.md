---
UID: NN:audioclient.IAudioCaptureClient
title: IAudioCaptureClient (audioclient.h)
author: windows-sdk-content
description: The IAudioCaptureClient interface enables a client to read input data from a capture endpoint buffer.
old-location: coreaudio\iaudiocaptureclient.htm
tech.root: CoreAudio
ms.assetid: c0fa6841-56bf-421e-9949-c6a037cf9fd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioCaptureClient, IAudioCaptureClient interface [Core Audio], IAudioCaptureClient interface [Core Audio],described, audioclient/IAudioCaptureClient, coreaudio.iaudiocaptureclient
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Audioclient.h
api_name:
 - IAudioCaptureClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioCaptureClient interface


## -description



The <b>IAudioCaptureClient</b> interface enables a client to read input data from a capture endpoint buffer. The client obtains a reference to the <b>IAudioCaptureClient</b> interface on a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioCaptureClient.

The methods in this interface manage the movement of data packets that contain capture data. The length of a data packet is expressed as the number of audio frames in the packet. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the W<b>AVEFORMATEX (or WAVEFORMATEXTENSIBLE)</b> structure that the client obtains by calling the <a href="https://msdn.microsoft.com/63f3e593-3904-44f9-a912-78c6c98e7597">IAudioClient::GetMixFormat</a> method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples. A packet always contains an integral number of audio frames.

When releasing an <b>IAudioCaptureClient</b> interface instance, the client must call the <b>Release</b> method of the instance from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

For a code example that uses the <b>IAudioCaptureClient</b> interface, see <a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioCaptureClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioCaptureClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioCaptureClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next available packet of data in the capture endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/352dcd7d-a7e1-493f-b9ce-c125f9d45fa8">GetNextPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames in the next data packet in the capture endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38e1ea6c-d07d-4075-b6f2-d563c4bce007">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases the buffer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/63f3e593-3904-44f9-a912-78c6c98e7597">IAudioClient::GetMixFormat</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

