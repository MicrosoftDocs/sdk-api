---
UID: NN:audiopolicy.IAudioSessionEnumerator
title: IAudioSessionEnumerator
author: windows-sdk-content
description: The IAudioSessionEnumerator interface enumerates audio sessions on an audio device.
old-location: coreaudio\iaudiosessionenumerator.htm
tech.root: CoreAudio
ms.assetid: a7976d13-3391-4747-b83a-cfb9407b34f2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IAudioSessionEnumerator, IAudioSessionEnumerator interface [Core Audio], IAudioSessionEnumerator interface [Core Audio],described, audiopolicy/IAudioSessionEnumerator, coreaudio.iaudiosessionenumerator
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
 - IAudioSessionEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEnumerator interface


## -description


The <b>IAudioSessionEnumerator</b> interface enumerates audio sessions on an audio device. To get a reference to the <b>IAudioSessionEnumerator</b> interface of the session enumerator object, the application must call <a href="https://msdn.microsoft.com/68166fc1-af27-4251-8e18-be23d205b567">IAudioSessionManager2::GetSessionEnumerator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSessionEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioSessionEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSessionEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1fbfbf5-a79b-40bc-97c7-a76a181bbfec">GetCount</a>
</td>
<td align="left" width="63%">
Gets the total number of audio sessions that are open on the audio device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45b7af16-aca0-49f8-b977-f7e4f1885687">GetSession</a>
</td>
<td align="left" width="63%">
Gets the audio session specified by an audio session number. 

</td>
</tr>
</table> 


## -remarks



If an application wants to be  notified when new sessions are created, it must register its implementation of  <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> with the session manager.  Upon successful registration, the session manager sends create-session notifications to the application in the form of callbacks. These notifications contain a reference to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer of the newly created session. 

The session enumerator maintains a list of current sessions by holding references to each session's <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer. However, the session enumerator might not be aware of the new sessions that are reported through <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>. In that case, the application would have access to only a partial list of sessions. This might occur if the <b>IAudioSessionControl</b> pointer (in the callback) is released before the session enumerator is initialized. Therefore,    if an application wants a complete set of sessions for the audio endpoint, the application should maintain its own list. 

The application must perform the following steps to receive session notifications and manage a list of current sessions.

<ol>
<li>Initialize COM with the Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager.  <div class="alert"><b>Note</b>  Threads that run the user interface of an application should be initialized with the apartment threading model.</div>
<div> </div>
</li>
<li>Activate an <a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a> interface from the audio endpoint device. Call <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> with parameter <i>iid</i> set to <b>IID_IAudioSessionManager2</b>. This call receives a reference to the session manager's <b>IAudioSessionManager2</b> interface in the <i>ppInterface</i> parameter.  </li>
<li>Implement the <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface to provide the callback behavior.</li>
<li>Call <a href="https://msdn.microsoft.com/cff43da7-70b2-4887-8a6c-6100cf7d696e">IAudioSessionManager2::RegisterSessionNotification</a> to register the application's implementation of  <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a>.</li>
<li>Create and initialize the session enumerator object by calling <a href="https://msdn.microsoft.com/68166fc1-af27-4251-8e18-be23d205b567">IAudioSessionManager2::GetSessionEnumerator</a>. This method generates a list of current sessions available for the endpoint and adds the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointers for  each session in the list, if they are not already present.</li>
<li>Use the <b>IAudioSessionEnumerator</b> interface returned in the previous step to retrieve and enumerate the list of sessions. The session control for each session can be retrieved by calling <a href="https://msdn.microsoft.com/45b7af16-aca0-49f8-b977-f7e4f1885687">IAudioSessionEnumerator::GetSession</a>. Make sure you call <b>AddRef</b> for each session control to maintain the reference count.</li>
<li>When the application gets a create-session notification, add  the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> pointer of the new session (received in <a href="https://msdn.microsoft.com/03f22e06-f446-4c57-a955-3d12deec4152">IAudioSessionNotification::OnSessionCreated</a>)  to the list of existing sessions. </li>
</ol>
Because the application maintains this list of sessions and manages the lifetime of the session based on the application's requirements, there is no expiration mechanism enforced by the audio system on the session control objects.

A session control is valid as long as the application has a reference to the session control in the list.  


#### Examples

The following example code shows how to create the session enumerator object and then enumerate sessions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumSessions(IAudioSessionManager2* pSessionManager)
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
    CHECK_HR( hr = pSessionManager-&gt;GetSessionEnumerator(&amp;pSessionList));
    
    // Get the session count.
    CHECK_HR( hr = pSessionList-&gt;GetCount(&amp;cbSessionCount));

    for (int index = 0 ; index &lt; cbSessionCount ; index++)
    {
        CoTaskMemFree(pswSession);
        SAFE_RELEASE(pSessionControl);
        
        // Get the &lt;n&gt;th session.
        CHECK_HR(hr = pSessionList-&gt;GetSession(index, &amp;pSessionControl));

        CHECK_HR(hr = pSessionControl-&gt;GetDisplayName(&amp;pswSession));

        wprintf_s(L"Session Name: %s\n", pswSession);
    }

done:
    CoTaskMemFree(pswSession);
    SAFE_RELEASE(pSessionControl);
    SAFE_RELEASE(pSessionList);

    return hr;

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

