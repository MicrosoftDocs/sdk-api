---
UID: NF:audioclient.IAudioClient.GetService
title: IAudioClient::GetService (audioclient.h)
description: The GetService method accesses additional services from the audio client object.
helpviewer_keywords: ["GetService","GetService method [Core Audio]","GetService method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetService method","IAudioClient.GetService","IAudioClient::GetService","IAudioClientGetService","audioclient/IAudioClient::GetService","coreaudio.iaudioclient_getservice"]
old-location: coreaudio\iaudioclient_getservice.htm
tech.root: CoreAudio
ms.assetid: 233d4471-037f-4df9-bef6-57f2544dedb5
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Core Audio], GetService method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetService method, IAudioClient.GetService, IAudioClient::GetService, IAudioClientGetService, audioclient/IAudioClient::GetService, coreaudio.iaudioclient_getservice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioClient::GetService
 - audioclient/IAudioClient::GetService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient.GetService
---

# IAudioClient::GetService


## -description

The <b>GetService</b> method accesses additional services from the audio client object.

## -parameters

### -param riid [in]

The interface ID for the requested service. The client should set this parameter to one of the following REFIID values:

IID_IAudioCaptureClient

IID_IAudioClientDuckingControl

IID_IAudioClock

IID_IAudioRenderClient

IID_IAudioSessionControl

IID_IAudioStreamVolume

IID_IChannelAudioVolume

IID_IMFTrustedOutput

IID_ISimpleAudioVolume



For more information, see Remarks.

### -param ppv [out]

Pointer to a pointer variable into which the method writes the address of an instance of the requested interface. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetService</b> call fails, <i>*ppv</i> is <b>NULL</b>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppv</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_WRONG_ENDPOINT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The caller tried to access an <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient</a> interface on a rendering endpoint, or an <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiorenderclient">IAudioRenderClient</a> interface on a capture endpoint.

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
<dt><b>AUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The stream's resources have been invalidated. This error may be thrown for the following reasons:<br>
- The stream is suspended.<br>
- An Exclusive or Offload stream is disconnected.<br>
- A packaged application that has an exclusive mode or offload stream is quiesced.<br>
- A "protected output" stream is closed.<br>
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

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

The <b>GetService</b> method supports the following service interfaces:

<ul>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiorenderclient">IAudioRenderClient</a>
</li>
<li>
<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput">IMFTrustedOutput</a>
</li>
<li>
<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a>
</li>
</ul>
In Windows 7, a new service identifier, <b>IID_IMFTrustedOutput</b>, has been added that facilitates the use of output trust authority (OTA) objects. These objects can operate inside or outside the Media Foundation's protected media path (PMP) and send content outside the Media Foundation pipeline. If the caller is outside PMP, then the OTA may not operate in the PMP,  and the protection settings are less robust. OTAs must implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput">IMFTrustedOutput</a> interface.
By passing <b>IID_IMFTrustedOutput</b> in <b>GetService</b>, an application can retrieve a pointer to the object's <b>IMFTrustedOutput</b> interface. For more information about protected objects and <b>IMFTrustedOutput</b>, see "Protected Media Path" in  the Media Foundation SDK documentation. 

For information about using trusted audio drivers in OTAs, see <a href="/windows/desktop/CoreAudio/protected-user-mode-audio--puma-">Protected User Mode Audio (PUMA)</a>.

Note that activating IMFTrustedOutput through this mechanism works regardless of whether the caller is running in PMP. However, if the caller is not running in a protected process (that is, the caller is not within Media Foundation's PMP) then the audio OTA might not operate in the PMP and the protection settings are less robust.

To obtain the interface ID for a service interface, use the <b>__uuidof</b> operator. For example, the interface ID of <b>IAudioCaptureClient</b> is defined as follows:


``` syntax

const IID IID_IAudioCaptureClient  __uuidof(IAudioCaptureClient)

```

For information about the <b>__uuidof</b> operator, see the Windows SDK documentation.

To release the <b>IAudioClient</b> object and free all its associated resources, the client must release all references to any service objects that were created by calling <b>GetService</b>, in addition to calling <b>Release</b> on the <b>IAudioClient</b> interface itself. The client must release a service from the same thread that releases the <b>IAudioClient</b> object.

The <b>IAudioSessionControl</b>, <b>IAudioStreamVolume</b>, <b>IChannelAudioVolume</b>, and <b>ISimpleAudioVolume</b> interfaces control and monitor aspects of audio sessions and shared-mode streams. These interfaces do not work with exclusive-mode streams.

For code examples that call the <b>GetService</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiocaptureclient">IAudioCaptureClient Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiorenderclient">IAudioRenderClient Interface</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>
