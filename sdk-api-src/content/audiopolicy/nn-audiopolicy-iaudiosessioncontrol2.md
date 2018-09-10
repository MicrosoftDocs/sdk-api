---
UID: NN:audiopolicy.IAudioSessionControl2
title: IAudioSessionControl2
author: windows-sdk-content
description: The IAudioSessionControl2 interface can be used by a client to get information about the audio session.
old-location: coreaudio\iaudiosessioncontrol2.htm
tech.root: CoreAudio
ms.assetid: 3bb65edf-103c-4eeb-82b4-7c571cddfcf3
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioSessionControl2, IAudioSessionControl2 interface [Core Audio], IAudioSessionControl2 interface [Core Audio],described, audiopolicy/IAudioSessionControl2, coreaudio.iaudiosessioncontrol2
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
 - IAudioSessionControl2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionControl2 interface


## -description


The     <b>IAudioSessionControl2</b> interface can be used by a client to get information about the audio session.

To get a reference to the <b>IAudioSessionControl2</b> interface, the application must call <b>IAudioSessionControl::QueryInterface</b> to request the interface pointer from the stream object's  <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> interface. There are two ways an application  can get a pointer to the <b>IAudioSessionControl</b> interface:
<ul>
<li>
By calling  <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> on the audio client after opening a stream on the device. The audio client opens a stream for rendering or capturing, and associates it with an audio session by calling <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.

</li>
<li>
By calling <a href="https://msdn.microsoft.com/42de66dd-46df-40af-9d8a-39ee9f91b468">IAudioSessionManager::GetAudioSessionControl</a> for an existing audio session without opening the stream.


</li>
</ul>When the application wants to release the <b>IAudioSessionControl2</b> interface instance, the application must call the interface's <b>Release</b> method from the same thread as the call to <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> that created the object.

The application thread that uses this interface must be initialized for COM. For more information about COM initialization, see the description of the <b>CoInitializeEx</b> function in the Windows SDK documentation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionControl2</b> interface inherits from <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a>. <b>IAudioSessionControl2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/17ae85ad-e2ef-4a87-9d0f-58baa080ff98">GetProcessId</a>
</td>
<td align="left" width="63%">
Retrieves the process identifier of the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1854e7fe-9d5f-42f3-9c4c-f2a27f26ac17">GetSessionIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02350812-7f05-400e-87f7-1d912a23050d">GetSessionInstanceIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the session instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9060f89c-83b1-433d-96e3-86ae4b1c7e7c">IsSystemSoundsSession</a>
</td>
<td align="left" width="63%">
Indicates whether the session is a system sounds session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6689d7e4-9c45-483d-9f46-14d157726b02">SetDuckingPreference</a>
</td>
<td align="left" width="63%">
Enables or disables the default stream attenuation experience (auto-ducking) provided by the system.

</td>
</tr>
</table> 


## -remarks



This interface supports  custom implementations for <i>stream attenuation</i> or <i>ducking</i>, a new feature in Windows 7. An application playing a media stream can make it behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. For more information about this feature, see <a href="https://msdn.microsoft.com/2ad9482f-1888-4f19-bc41-9d47a8e0ed15">Default Ducking Experience</a>. 

An application can use this interface to perform the following tasks:

<ul>
<li>Specify that it wants to opt out of the default stream attenuation experience provided by the system.</li>
<li>Get the audio session identifier that is associated with the stream. The identifier is required during the notification registration. The application can register itself to receive ducking notifications from the system.</li>
<li>Check whether the stream associated with the audio session  is a system sound.</li>
</ul>

#### Examples

The following example code shows how to get a reference to the <b>IAudioSessionControl2</b> interface and call its methods to determine whether the stream associated with the audio session is a system sound.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT SetDuckingForSystemSounds()
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
        (void**)&amp;pEnumerator));

    // Get the default audio device.
    CHECK_HR( hr = pEnumerator-&gt;GetDefaultAudioEndpoint(
                    eRender, eConsole, &amp;pDevice));

    // Get the audio client.
    CHECK_HR( hr = pDevice-&gt;Activate(
        __uuidof(IID_IAudioSessionManager), CLSCTX_ALL,
        NULL, (void**)&amp;pSessionManager));

    // Get a reference to the session manager.
    CHECK_HR( hr = pSessionManager-&gt;GetAudioSessionControl (GUID_NULL, FALSE, &amp;pSessionControl));
    
    // Get the extended session control interface pointer.
    CHECK_HR( hr = pSessionControl-&gt;QueryInterface(
        __uuidof(IAudioSessionControl2), (void**) &amp;pSessionControl2));

    // Check whether this is a system sound.
    CHECK_HR( hr = pSessionControl2-&gt;IsSystemSoundsSession());

    // If it is a system sound, opt out of the default
    // stream attenuation experience.
    CHECK_HR( hr = pSessionControl2-&gt;SetDuckingPreference(TRUE));

done:

    // Clean up.
    SAFE_RELEASE(pSessionControl2);
    SAFE_RELEASE(pSessionControl);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);


    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a>



<a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>
 

 

