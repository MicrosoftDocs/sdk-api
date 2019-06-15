---
UID: NN:audioclient.IAudioClient
title: IAudioClient (audioclient.h)
author: windows-sdk-content
description: The IAudioClient interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an audio endpoint device (for an exclusive-mode stream).
old-location: coreaudio\iaudioclient.htm
tech.root: CoreAudio
ms.assetid: 5088a3f1-5001-4ed9-a495-9e91df613ab0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioClient, IAudioClient interface [Core Audio], IAudioClient interface [Core Audio],described, audioclient/IAudioClient, coreaudio.iaudioclient
ms.topic: interface
f1_keywords: ["audioclient/IAudioClient"]
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
 - IAudioClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioClient interface


## -description



The <b>IAudioClient</b> interface enables a client to create and initialize an audio stream between an audio application and the audio engine (for a shared-mode stream) or the hardware buffer of an <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a> (for an exclusive-mode stream). A client obtains a reference to an <b>IAudioClient</b> interface for an audio endpoint device by following these steps:<ol>
<li>By using one of the techniques described in <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioClient.</li>
</ol>


The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.

For code examples that use the <b>IAudioClient</b> interface, see the following topics:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClient</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getbuffersize">GetBufferSize</a>
</td>
<td align="left" width="63%">
Retrieves the size (maximum capacity) of the audio buffer associated with the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getcurrentpadding">GetCurrentPadding</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames of padding in the endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getdeviceperiod">GetDevicePeriod</a>
</td>
<td align="left" width="63%">
Retrieves the length of the periodic interval separating successive processing passes by the audio engine on the data in the endpoint buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">GetMixFormat</a>
</td>
<td align="left" width="63%">
Retrieves the stream format that the audio engine uses for its internal processing of shared-mode streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">GetService</a>
</td>
<td align="left" width="63%">
Accesses additional services from the audio client object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getstreamlatency">GetStreamLatency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency for the current stream and can be called any time after the stream has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-isformatsupported">IsFormatSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the audio endpoint device supports a particular stream format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-seteventhandle">SetEventHandle</a>
</td>
<td align="left" width="63%">
Sets the event handle that the audio engine will signal each time a buffer becomes ready to be processed by the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">Start</a>
</td>
<td align="left" width="63%">
Starts the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">Stop</a>
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




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a>
 

 

