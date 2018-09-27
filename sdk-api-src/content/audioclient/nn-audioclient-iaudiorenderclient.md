---
UID: NN:audioclient.IAudioRenderClient
title: IAudioRenderClient
author: windows-sdk-content
description: The IAudioRenderClient interface enables a client to write output data to a rendering endpoint buffer.
old-location: coreaudio\iaudiorenderclient.htm
tech.root: CoreAudio
ms.assetid: e3e18e1e-1a09-4072-add6-36d2a6428a74
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAudioRenderClient, IAudioRenderClient interface [Core Audio], IAudioRenderClient interface [Core Audio],described, audioclient/IAudioRenderClient, coreaudio.iaudiorenderclient
ms.prod: windows
ms.technology: windows-sdk
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
 - IAudioRenderClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioRenderClient interface


## -description



The <b>IAudioRenderClient</b> interface enables a client to write output data to a rendering endpoint buffer. The client obtains a reference to the <b>IAudioRenderClient</b> interface of a stream object by calling the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_IAudioRenderClient.

The methods in this interface manage the movement of data packets that contain audio-rendering data. The length of a data packet is expressed as the number of audio frames in the packet. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the <b>WAVEFORMATEX</b> structure that the client obtains by calling the <a href="https://msdn.microsoft.com/63f3e593-3904-44f9-a912-78c6c98e7597">IAudioClient::GetMixFormat</a> method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples. A packet always contains an integral number of audio frames.

When releasing an <b>IAudioRenderClient</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

For code examples that use the <b>IAudioRenderClient</b> interface, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/196cc6fe-91bf-46fa-acc9-38a7a4005875">Exclusive-Mode Streams</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioRenderClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioRenderClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioRenderClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next available space in the rendering endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19d89b5e-2e73-4693-b970-7ebf452ef9a1">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases the buffer space acquired in the previous call to the <a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">IAudioRenderClient::GetBuffer</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/63f3e593-3904-44f9-a912-78c6c98e7597">IAudioClient::GetMixFormat</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

