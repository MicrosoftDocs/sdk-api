---
UID: NF:audioclient.IAudioClient.GetBufferSize
title: IAudioClient::GetBufferSize
author: windows-sdk-content
description: The GetBufferSize method retrieves the size (maximum capacity) of the endpoint buffer.
old-location: coreaudio\iaudioclient_getbuffersize.htm
old-project: CoreAudio
ms.assetid: 562d2db6-ae14-47c9-8b8f-d4d90072b3dd
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetBufferSize, GetBufferSize method [Core Audio], GetBufferSize method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetBufferSize method, IAudioClient.GetBufferSize, IAudioClient::GetBufferSize, IAudioClientGetBufferSize, audioclient/IAudioClient::GetBufferSize, coreaudio.iaudioclient_getbuffersize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.redist: 
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
 - IAudioClient.GetBufferSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient::GetBufferSize


## -description



The <b>GetBufferSize</b> method retrieves the size (maximum capacity) of the endpoint buffer.




## -parameters




### -param pNumBufferFrames [out]

Pointer to a <b>UINT32</b> variable into which the method writes the number of audio frames that the buffer can hold.


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
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pNumBufferFrames</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method requires prior initialization of the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method.

This method retrieves the length of the endpoint buffer shared between the client application and the audio engine. The length is expressed as the number of audio frames the buffer can hold. The size in bytes of an audio frame is calculated as the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples.

The <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method allocates the buffer. The client specifies the buffer length in the <i>hnsBufferDuration</i> parameter value that it passes to the <b>Initialize</b> method. For rendering clients, the buffer length determines the maximum amount of rendering data that the application can write to the endpoint buffer during a single processing pass. For capture clients, the buffer length determines the maximum amount of capture data that the audio engine can read from the endpoint buffer during a single processing pass. The client should always call <b>GetBufferSize</b> after calling <b>Initialize</b> to determine the actual size of the allocated buffer, which might differ from the requested size.

Rendering clients can use this value to calculate the largest rendering buffer size that can be requested from <a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">IAudioRenderClient::GetBuffer</a> during each processing pass.

For code examples that call the <b>GetBufferSize</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">IAudioRenderClient::GetBuffer</a>
 

 

