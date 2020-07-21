---
UID: NN:audiopolicy.IAudioSessionControl2
title: IAudioSessionControl2 (audiopolicy.h)
description: The IAudioSessionControl2 interface can be used by a client to get information about the audio session.
helpviewer_keywords: ["IAudioSessionControl2","IAudioSessionControl2 interface [Core Audio]","IAudioSessionControl2 interface [Core Audio]","described","audiopolicy/IAudioSessionControl2","coreaudio.iaudiosessioncontrol2"]
old-location: coreaudio\iaudiosessioncontrol2.htm
tech.root: CoreAudio
ms.assetid: 3bb65edf-103c-4eeb-82b4-7c571cddfcf3
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl2, IAudioSessionControl2 interface [Core Audio], IAudioSessionControl2 interface [Core Audio],described, audiopolicy/IAudioSessionControl2, coreaudio.iaudiosessioncontrol2
f1_keywords:
- audiopolicy/IAudioSessionControl2
dev_langs:
- c++
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- audiopolicy.h
api_name:
- IAudioSessionControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioSessionControl2 interface


## -description


The     <b>IAudioSessionControl2</b> interface can be used by a client to get information about the audio session.

To get a reference to the <b>IAudioSessionControl2</b> interface, the application must call <b>IAudioSessionControl::QueryInterface</b> to request the interface pointer from the stream object's  <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> interface. There are two ways an application  can get a pointer to the <b>IAudioSessionControl</b> interface:
<ul>
<li>
By calling  <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> on the audio client after opening a stream on the device. The audio client opens a stream for rendering or capturing, and associates it with an audio session by calling <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

</li>
<li>
By calling <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol">IAudioSessionManager::GetAudioSessionControl</a> for an existing audio session without opening the stream.


</li>
</ul>When the application wants to release the <b>IAudioSessionControl2</b> interface instance, the application must call the interface's <b>Release</b> method from the same thread as the call to <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> that created the object.

The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionControl2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a>. <b>IAudioSessionControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getprocessid">GetProcessId</a>
</td>
<td align="left" width="63%">
Retrieves the process identifier of the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessionidentifier">GetSessionIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier">GetSessionInstanceIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the session instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-issystemsoundssession">IsSystemSoundsSession</a>
</td>
<td align="left" width="63%">
Indicates whether the session is a system sounds session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference">SetDuckingPreference</a>
</td>
<td align="left" width="63%">
Enables or disables the default stream attenuation experience (auto-ducking) provided by the system.

</td>
</tr>
</table> 


## -remarks



This interface supports  custom implementations for <i>stream attenuation</i> or <i>ducking</i>, a new feature in Windows 7. An application playing a media stream can make it behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. For more information about this feature, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/stream-attenuation">Default Ducking Experience</a>. 

An application can use this interface to perform the following tasks:

<ul>
<li>Specify that it wants to opt out of the default stream attenuation experience provided by the system.</li>
<li>Get the audio session identifier that is associated with the stream. The identifier is required during the notification registration. The application can register itself to receive ducking notifications from the system.</li>
<li>Check whether the stream associated with the audio session  is a system sound.</li>
</ul>

#### Examples

The following example code shows how to get a reference to the <b>IAudioSessionControl2</b> interface and call its methods to determine whether the stream associated with the audio session is a system sound.


```cpp
HRESULT SetDuckingForSystemSounds()
{
 
    HRESULT hr = S_OK;
    
    IMMDevice* pDevice = NULL;
    IMMDeviceEnumerator* pEnumerator = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;
    IAudioSessionManager* pSessionManager = NULL;

    CHECK_HR( hr = CoInitialize(NULL));

    // Create the device enumerator.
    CHECK_HR( hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator), 
        NULL, CLSCTX_ALL, 
        __uuidof(IMMDeviceEnumerator), 
        (void**)&pEnumerator));

    // Get the default audio device.
    CHECK_HR( hr = pEnumerator->GetDefaultAudioEndpoint(
                    eRender, eConsole, &pDevice));

    // Get the audio client.
    CHECK_HR( hr = pDevice->Activate(
        __uuidof(IID_IAudioSessionManager), CLSCTX_ALL,
        NULL, (void**)&pSessionManager));

    // Get a reference to the session manager.
    CHECK_HR( hr = pSessionManager->GetAudioSessionControl (GUID_NULL, FALSE, &pSessionControl));
    
    // Get the extended session control interface pointer.
    CHECK_HR( hr = pSessionControl->QueryInterface(
        __uuidof(IAudioSessionControl2), (void**) &pSessionControl2));

    // Check whether this is a system sound.
    CHECK_HR( hr = pSessionControl2->IsSystemSoundsSession());

    // If it is a system sound, opt out of the default
    // stream attenuation experience.
    CHECK_HR( hr = pSessionControl2->SetDuckingPreference(TRUE));

done:

    // Clean up.
    SAFE_RELEASE(pSessionControl2);
    SAFE_RELEASE(pSessionControl);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);


    return hr;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>
 

 

