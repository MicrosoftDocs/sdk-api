---
UID: NF:audioclient.IAudioClient.Reset
title: IAudioClient::Reset
author: windows-sdk-content
description: The Reset method resets the audio stream.
old-location: coreaudio\iaudioclient_reset.htm
tech.root: CoreAudio
ms.assetid: c1a4f673-ecbf-4855-b8bb-c0f0807dedd4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAudioClient interface [Core Audio],Reset method, IAudioClient.Reset, IAudioClient::Reset, IAudioClientReset, Reset, Reset method [Core Audio], Reset method [Core Audio],IAudioClient interface, audioclient/IAudioClient::Reset, coreaudio.iaudioclient_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAudioClient.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioClient::Reset


## -description



The <b>Reset</b> method resets the audio stream.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If the method succeeds and the stream was already reset, the method returns S_FALSE. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>AUDCLNT_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream was not stopped at the time the call was made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_OPERATION_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The client is currently writing to or reading from the buffer.

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



This method requires prior initialization of the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method.

<b>Reset</b> is a control method that the client calls to reset a stopped audio stream. Resetting the stream flushes all pending data and resets the audio clock stream position to 0. This method fails if it is called on a stream that is not stopped.




## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>
 

 

