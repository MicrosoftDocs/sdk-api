---
UID: NN:audiopolicy.IAudioSessionManager2
title: IAudioSessionManager2 (audiopolicy.h)
description: The IAudioSessionManager2 interface enables an application to manage submixes for the audio device.
helpviewer_keywords: ["IAudioSessionManager2","IAudioSessionManager2 interface [Core Audio]","IAudioSessionManager2 interface [Core Audio]","described","audiopolicy/IAudioSessionManager2","coreaudio.iaudiosessionmanager2"]
old-location: coreaudio\iaudiosessionmanager2.htm
tech.root: CoreAudio
ms.assetid: 476dac90-d0c4-499c-973e-33ea55546659
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager2, IAudioSessionManager2 interface [Core Audio], IAudioSessionManager2 interface [Core Audio],described, audiopolicy/IAudioSessionManager2, coreaudio.iaudiosessionmanager2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSessionManager2
 - audiopolicy/IAudioSessionManager2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionManager2
---

# IAudioSessionManager2 interface


## -description

The <b>IAudioSessionManager2</b> interface enables an application to manage submixes for the audio device.

To a get a reference to an <b>IAudioSessionManager2</b> interface, the application must activate it on the audio device by following these steps:<ol>
<li>Use one of the techniques described on the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface page to obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device. 
</li>
<li>Call the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to IID_IAudioSessionManager2. </li>
</ol>


When the application wants to release the <b>IAudioSessionManager2</b> interface instance, the application must call the interface's <b>Release</b> method.

The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.

## -inheritance

The <b>IAudioSessionManager2</b> interface inherits from <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager">IAudioSessionManager</a>. <b>IAudioSessionManager2</b> also has these types of members:

## -remarks

An application can use this interface to perform the following tasks:

<ul>
<li>Register to receive ducking notifications.</li>
<li>Register to receive a notification  when a  session is created.</li>
<li>Enumerate sessions on the audio device that was used to get the interface pointer. </li>
</ul>


This interface supports  custom implementations for <i>stream attenuation</i> or <i>ducking</i>, a new feature in Windows 7. An application playing a media stream can make the it behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. For more information about this feature, see <a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>.

An application that manages the media streams and wants to provide a custom ducking implementation, must register to receive notifications when session events occur. For stream attenuation, a session event is raised by the system when a communication stream is opened or closed on the default communication device. For more information, see <a href="/windows/desktop/CoreAudio/providing-a-custom-ducking-experience">Providing a Custom Ducking Behavior</a>.


#### Examples

The following example code shows how to get a reference to the <b>IAudioSessionManager2</b> interface of the audio device.


```cpp
HRESULT CreateSessionManager(IAudioSessionManager2** ppSessionManager)
{
 
    HRESULT hr = S_OK;
    
    IMMDevice* pDevice = NULL;
    IMMDeviceEnumerator* pEnumerator = NULL;
    IAudioSessionManager2* pSessionManager = NULL;


    // Create the device enumerator.
    CHECK_HR( hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator), 
        NULL, CLSCTX_ALL, 
        __uuidof(IMMDeviceEnumerator), 
        (void**)&pEnumerator));

    // Get the default audio device.
    CHECK_HR( hr = pEnumerator->GetDefaultAudioEndpoint(
                    eRender, eConsole, &pDevice));

    // Get the session manager.
    CHECK_HR( hr = pDevice->Activate(
        __uuidof(IAudioSessionManager2), CLSCTX_ALL,
        NULL, (void**)&pSessionManager));

    // Return the pointer to the caller.
    *(ppSessionManager) = pSessionManager;
    (*ppSessionManager)->AddRef();

done:

    // Clean up.
    SAFE_RELEASE(pSessionManager);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);

    return hr;
}
```

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager">IAudioSessionManager</a>
