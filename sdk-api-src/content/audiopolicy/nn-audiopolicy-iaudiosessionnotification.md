---
UID: NN:audiopolicy.IAudioSessionNotification
title: IAudioSessionNotification (audiopolicy.h)
description: The IAudioSessionNotification interface provides notification when an audio session is created.
helpviewer_keywords: ["IAudioSessionNotification","IAudioSessionNotification interface [Core Audio]","IAudioSessionNotification interface [Core Audio]","described","audiopolicy/IAudioSessionNotification","coreaudio.iaudiosessionnotification"]
old-location: coreaudio\iaudiosessionnotification.htm
tech.root: CoreAudio
ms.assetid: 69222168-87d7-4f5a-93b1-6d91263a54bd
ms.date: 12/05/2018
ms.keywords: IAudioSessionNotification, IAudioSessionNotification interface [Core Audio], IAudioSessionNotification interface [Core Audio],described, audiopolicy/IAudioSessionNotification, coreaudio.iaudiosessionnotification
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
 - IAudioSessionNotification
 - audiopolicy/IAudioSessionNotification
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
 - IAudioSessionNotification
---

# IAudioSessionNotification interface


## -description

The <b>IAudioSessionNotification</b> interface provides  notification when an audio session is created.

## -inheritance

The <b>IAudioSessionNotification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionNotification</b> also has these types of members:

## -remarks

Unlike the other WASAPI interfaces, which are implemented by the WASAPI system component, the <b>IAudioSessionNotification</b> interface is implemented by the application. To receive event notifications, the application passes to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registersessionnotification">IAudioSessionManager2::RegisterSessionNotification</a> method a pointer to its <b>IAudioSessionNotification</b> implementation .


After registering its <b>IAudioSessionNotification</b> interface, the application receives event notifications in the form of callbacks through the methods in the interface.

When the application no longer needs to receive notifications, it calls the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregistersessionnotification">IAudioSessionManager2::UnregisterSessionNotification</a> method. This method removes the registration of an <b>IAudioSessionNotification</b> interface that the application previously registered.

The application must not register or unregister notification callbacks during an event callback. 


The session enumerator might not be aware of the new sessions that are reported through <b>IAudioSessionNotification</b>. So if an application exclusively relies on the session enumerator for getting all the sessions for an audio endpoint, the results might not be accurate. To work around this, the application should manually maintain a list. For more information, see <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator</a>.

<div class="alert"><b>Note</b>  Make sure that the application initializes COM with Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager. 
Threads that run the user interface of an application should be initialized apartment threading model.

</div>
<div> </div>

#### Examples

The following code example shows a sample implementation of the <b>IAudioSessionNotification</b> interface.


```cpp
class CSessionNotifications: public IAudioSessionNotification
{
private:

    LONG             m_cRefAll;
    HWND m_hwndMain;

    ~CSessionManager(){};

public:


    CSessionManager(HWND hWnd): 
    m_cRefAll(1),
    m_hwndMain (hWnd)

    {}

    // IUnknown
    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void **ppv)  
    {    
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionNotification) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionNotification*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }
    
    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&m_cRefAll);
    }
     
    ULONG STDMETHODCALLTYPE Release)()
    {
        ULONG ulRef = InterlockedDecrement(&m_cRefAll);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT OnSessionCreated(IAudioSessionControl *pNewSession)
    {
        if (pNewSession)
        {
            PostMessage(m_hwndMain, WM_SESSION_CREATED, 0, 0);
        }
    }
};
```

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
