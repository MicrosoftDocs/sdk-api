---
UID: NN:audioclient.IAudioClient
title: IAudioClient
author: windows-sdk-content
description: The IAudioClient interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an audio endpoint device (for an exclusive-mode stream).
old-location: coreaudio\iaudioclient.htm
old-project: CoreAudio
ms.assetid: 5088a3f1-5001-4ed9-a495-9e91df613ab0
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IAudioClient, IAudioClient interface [Core Audio], IAudioClient interface [Core Audio],described, audioclient/IAudioClient, coreaudio.iaudioclient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient interface


## -description



The <b>IAudioClient</b> interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint device</a> (for an exclusive-mode stream). A client obtains a reference to an <b>IAudioClient</b> interface for an audio endpoint device by following these steps:<ol>
<li>By using one of the techniques described in <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioClient.</li>
</ol>


The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.

For code examples that use the <b>IAudioClient</b> interface, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/196cc6fe-91bf-46fa-acc9-38a7a4005875">Exclusive-Mode Streams</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/562d2db6-ae14-47c9-8b8f-d4d90072b3dd">GetBufferSize</a>
</td>
<td align="left" width="63%">
Retrieves the size (maximum capacity) of the audio buffer associated with the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a2c9ddf-f668-41ff-85f0-34de593c0fe2">GetCurrentPadding</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames of padding in the endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2f75fce-9eca-488d-b183-87d97d4e599a">GetDevicePeriod</a>
</td>
<td align="left" width="63%">
Retrieves the length of the periodic interval separating successive processing passes by the audio engine on the data in the endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265084">GetMixFormat</a>
</td>
<td align="left" width="63%">
Retrieves the stream format that the audio engine uses for its internal processing of shared-mode streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">GetService</a>
</td>
<td align="left" width="63%">
Accesses additional services from the audio client object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccc06e31-e56f-4910-882a-40b1ce0b43aa">GetStreamLatency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency for the current stream and can be called any time after the stream has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92d1fc93-08e2-46d9-bd2f-ce1b2087d2d1">IsFormatSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the audio endpoint device supports a particular stream format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bca0c00-5157-43bf-98bd-3bfb23abe860">SetEventHandle</a>
</td>
<td align="left" width="63%">
Sets the event handle that the audio engine will signal each time a buffer becomes ready to be processed by the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the audio stream.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  In Windows 8, the first use of <b>IAudioClient</b> to access the audio device should be on the STA thread. Calls from an MTA thread may result in undefined behavior.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>



<a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a>
 

 

