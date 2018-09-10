---
UID: NN:audiopolicy.IAudioSessionManager2
title: IAudioSessionManager2
author: windows-sdk-content
description: The IAudioSessionManager2 interface enables an application to manage submixes for the audio device.
old-location: coreaudio\iaudiosessionmanager2.htm
tech.root: CoreAudio
ms.assetid: 476dac90-d0c4-499c-973e-33ea55546659
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioSessionManager2, IAudioSessionManager2 interface [Core Audio], IAudioSessionManager2 interface [Core Audio],described, audiopolicy/IAudioSessionManager2, coreaudio.iaudiosessionmanager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IAudioSessionManager2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionManager2 interface


## -description


The <b>IAudioSessionManager2</b> interface enables an application to manage submixes for the audio device.

To a get a reference to an <b>IAudioSessionManager2</b> interface, the application must activate it on the audio device by following these steps:<ol>
<li>Use one of the techniques described on the <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface page to obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device. 
</li>
<li>Call the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>iid</i> set to IID_IAudioSessionManager2. </li>
</ol>


When the application wants to release the <b>IAudioSessionManager2</b> interface instance, the application must call the interface's <b>Release</b> method.

The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionManager2</b> interface inherits from <a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a>. <b>IAudioSessionManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68166fc1-af27-4251-8e18-be23d205b567">GetSessionEnumerator</a>
</td>
<td align="left" width="63%">
Gets a pointer to the audio session enumerator object used to enumerate sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bed27f3f-6293-4a25-baa0-39562d45bddc">RegisterDuckNotification</a>
</td>
<td align="left" width="63%">
Registers the application to receive ducking notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cff43da7-70b2-4887-8a6c-6100cf7d696e">RegisterSessionNotification</a>
</td>
<td align="left" width="63%">
Registers the application to receive a notification when a session is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ab0f5d0-8831-41a2-bfee-3e88a3d92156">UnregisterDuckNotification</a>
</td>
<td align="left" width="63%">
Deletes the registration to  receive ducking notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c334963-2b60-4eb1-b8a2-c9ed0d21bd5e">UnregisterSessionNotification</a>
</td>
<td align="left" width="63%">
Deletes the registration to  receive a notification when a session is created.

</td>
</tr>
</table> 


## -remarks




An application can use this interface to perform the following tasks:

<ul>
<li>Register to receive ducking notifications.</li>
<li>Register to receive a notification  when a  session is created.</li>
<li>Enumerate sessions on the audio device that was used to get the interface pointer. </li>
</ul>


This interface supports  custom implementations for <i>stream attenuation</i> or <i>ducking</i>, a new feature in Windows 7. An application playing a media stream can make the it behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. For more information about this feature, see <a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>.

An application that manages the media streams and wants to provide a custom ducking implementation, must register to receive notifications when session events occur. For stream attenuation, a session event is raised by the system when a communication stream is opened or closed on the default communication device. For more information, see <a href="https://msdn.microsoft.com/18290d05-b114-476b-8365-6bbb5fe6cffc">Providing a Custom Ducking Behavior</a>.


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




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a>
 

 

