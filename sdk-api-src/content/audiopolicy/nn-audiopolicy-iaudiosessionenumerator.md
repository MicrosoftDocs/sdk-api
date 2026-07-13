---
UID: NN:audiopolicy.IAudioSessionEnumerator
title: IAudioSessionEnumerator (audiopolicy.h)
description: The IAudioSessionEnumerator interface enumerates audio sessions on an audio device.
helpviewer_keywords: ["IAudioSessionEnumerator","IAudioSessionEnumerator interface [Core Audio]","IAudioSessionEnumerator interface [Core Audio]","described","audiopolicy/IAudioSessionEnumerator","coreaudio.iaudiosessionenumerator"]
old-location: coreaudio\iaudiosessionenumerator.htm
tech.root: CoreAudio
ms.assetid: a7976d13-3391-4747-b83a-cfb9407b34f2
ms.date: 12/05/2018
ms.keywords: IAudioSessionEnumerator, IAudioSessionEnumerator interface [Core Audio], IAudioSessionEnumerator interface [Core Audio],described, audiopolicy/IAudioSessionEnumerator, coreaudio.iaudiosessionenumerator
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
 - IAudioSessionEnumerator
 - audiopolicy/IAudioSessionEnumerator
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
 - IAudioSessionEnumerator
---

# IAudioSessionEnumerator interface


## -description

The <b>IAudioSessionEnumerator</b> interface enumerates audio sessions on an audio device. To get a reference to the <b>IAudioSessionEnumerator</b> interface of the session enumerator object, the application must call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-getsessionenumerator">IAudioSessionManager2::GetSessionEnumerator</a>.

## -inheritance

The <b>IAudioSessionEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionEnumerator</b> also has these types of members:

## -remarks

If an application wants to be  notified when new sessions are created, it must register its implementation of  <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> with the session manager.  Upon successful registration, the session manager sends create-session notifications to the application in the form of callbacks. These notifications contain a reference to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> pointer of the newly created session. 

The session enumerator maintains a list of current sessions by holding references to each session's <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> pointer. However, the session enumerator might not be aware of the new sessions that are reported through <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a>. In that case, the application would have access to only a partial list of sessions. This might occur if the <b>IAudioSessionControl</b> pointer (in the callback) is released before the session enumerator is initialized. Therefore,    if an application wants a complete set of sessions for the audio endpoint, the application should maintain its own list. 

The application must perform the following steps to receive session notifications and manage a list of current sessions.

<ol>
<li>Initialize COM with the Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager.  <div class="alert"><b>Note</b>  Threads that run the user interface of an application should be initialized with the apartment threading model.</div>
<div> </div>
</li>
<li>Activate an <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a> interface from the audio endpoint device. Call <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> with parameter <i>iid</i> set to <b>IID_IAudioSessionManager2</b>. This call receives a reference to the session manager's <b>IAudioSessionManager2</b> interface in the <i>ppInterface</i> parameter.  </li>
<li>Implement the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface to provide the callback behavior.</li>
<li>Call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registersessionnotification">IAudioSessionManager2::RegisterSessionNotification</a> to register the application's implementation of  <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a>.</li>
<li>Create and initialize the session enumerator object by calling <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-getsessionenumerator">IAudioSessionManager2::GetSessionEnumerator</a>. This method generates a list of current sessions available for the endpoint and adds the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> pointers for  each session in the list, if they are not already present.</li>
<li>Use the <b>IAudioSessionEnumerator</b> interface returned in the previous step to retrieve and enumerate the list of sessions. The session control for each session can be retrieved by calling <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionenumerator-getsession">IAudioSessionEnumerator::GetSession</a>. Make sure you call <b>AddRef</b> for each session control to maintain the reference count.</li>
<li>When the application gets a create-session notification, add  the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> pointer of the new session (received in <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionnotification-onsessioncreated">IAudioSessionNotification::OnSessionCreated</a>)  to the list of existing sessions. </li>
</ol>
Because the application maintains this list of sessions and manages the lifetime of the session based on the application's requirements, there is no expiration mechanism enforced by the audio system on the session control objects.

A session control is valid as long as the application has a reference to the session control in the list.  


#### Examples

The following example code shows how to create the session enumerator object and then enumerate sessions.


```cpp
HRESULT EnumSessions(IAudioSessionManager2* pSessionManager)
{
    if (!pSessionManager)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;
    
    int cbSessionCount = 0;
    LPWSTR pswSession = NULL;
    
    IAudioSessionEnumerator* pSessionList = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    
    // Get the current list of sessions.
    CHECK_HR( hr = pSessionManager->GetSessionEnumerator(&pSessionList));
    
    // Get the session count.
    CHECK_HR( hr = pSessionList->GetCount(&cbSessionCount));

    for (int index = 0 ; index < cbSessionCount ; index++)
    {
        CoTaskMemFree(pswSession);
        SAFE_RELEASE(pSessionControl);
        
        // Get the <n>th session.
        CHECK_HR(hr = pSessionList->GetSession(index, &pSessionControl));

        CHECK_HR(hr = pSessionControl->GetDisplayName(&pswSession));

        wprintf_s(L"Session Name: %s\n", pswSession);
    }

done:
    CoTaskMemFree(pswSession);
    SAFE_RELEASE(pSessionControl);
    SAFE_RELEASE(pSessionList);

    return hr;

}
```

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
