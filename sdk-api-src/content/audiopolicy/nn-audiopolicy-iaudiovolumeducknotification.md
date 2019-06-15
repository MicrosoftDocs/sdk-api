---
UID: NN:audiopolicy.IAudioVolumeDuckNotification
title: IAudioVolumeDuckNotification (audiopolicy.h)
author: windows-sdk-content
description: The IAudioVolumeDuckNotification interface is used to by the system to send notifications about stream attenuation changes.Stream Attenuation, or ducking, is a feature introduced in Windows 7, where the system adjusts the volume of a non-communication stream when a new communication stream is opened. For more information about this feature, see Default Ducking Experience.
old-location: coreaudio\iaudiovolumeducknotification.htm
tech.root: CoreAudio
ms.assetid: 08e90a50-a6ac-4405-ba90-a862b78efaf8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioVolumeDuckNotification, IAudioVolumeDuckNotification interface [Core Audio], IAudioVolumeDuckNotification interface [Core Audio],described, audiopolicy/ IAudioVolumeDuckNotification, coreaudio.iaudiovolumeducknotification
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
 - AudioPolicy.h
api_name:
 - IAudioVolumeDuckNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioVolumeDuckNotification interface


## -description


The <b>IAudioVolumeDuckNotification</b> interface is used to by the system to send notifications about stream attenuation changes.Stream Attenuation, or ducking, is a feature introduced in Windows 7, where the system adjusts the volume of a non-communication stream when a new communication stream is opened. For more information about this feature, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/stream-attenuation">Default Ducking Experience</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IAudioVolumeDuckNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b> IAudioVolumeDuckNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b> IAudioVolumeDuckNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification">OnVolumeDuckNotification</a>
</td>
<td align="left" width="63%">
Sends a notification about a pending system ducking event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification">OnVolumeUnduckNotification</a>
</td>
<td align="left" width="63%">
Sends a notification about a pending system unducking event.

</td>
</tr>
</table> 


## -remarks



    If an application needs to opt out of the system attenuation experience provided by the system, it must call <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference">IAudioSessionControl2::SetDuckingPreference</a> and specify that preference. 

Unlike the other WASAPI interfaces, which are implemented by the WASAPI system component, the <b>IAudioVolumeDuckNotification</b> interface is implemented by the application to provide custom stream attenuation behavior. To receive event notifications, the application passes to the <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification">IAudioSessionManager2::RegisterDuckNotification</a> method a pointer to the application's implementation of <b>IAudioVolumeDuckNotification</b>.

After the application has registered its <b>IAudioVolumeDuckNotification</b> interface, the session manager calls the <b>IAudioVolumeDuckNotification</b> implementation when it needs to send ducking notifications. The application receives event notifications in the form of callbacks through the methods of the interface.

When the application no longer needs to receive notifications, it calls the <a href="https://docs.microsoft.com/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification">IAudioSessionManager2::UnregisterDuckNotification</a> method. The <b>UnregisterDuckNotification</b> method removes the registration of an <b>IAudioVolumeDuckNotification</b> interface that the application previously registered.

The application must not register or unregister notification callbacks during an event callback. 



For more information, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/handling-audio-ducking-events-from-communication-devices">Implementation Considerations for Ducking Notifications</a>.


#### Examples

The following example code shows a sample implementation of the <b>IAudioVolumeDuckNotification</b> interface.


```cpp


class CDuckNotification : public IAudioVolumeDuckNotification
{
    LONG            _Cref;
    HWND            m_hwndMain;

    CDuckNotification (HWND hWnd) : 
        _Cref(1), 
        m_hwndMain (hWnd)
							 {}

    
    HRESULT OnVolumeDuckNotification (LPCWSTR SessionID, UINT32 CommunicationSessionCount)
    {
         PostMessage(m_hwndMain, WM_VOLUME_DUCK, 0, 0);
         return S_OK;
    }
    HRESULT OnVolumeUnduckNotification (LPCWSTR SessionID)
    {
         PostMessage(m_hwndMain, WM_VOLUME_UNDUCK, 0, 0);
         return S_OK;
    }

protected:
    ~CDuckNotification() {}

public:
    HRESULT QueryInterface (REFIID Iid, void** ReturnValue)
    {
        if (ReturnValue == NULL)
        {
            return E_POINTER;
        }
        *ReturnValue = NULL;
        if (iid == IID_IUnknown)
        {
            *ReturnValue = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>(this));
            AddRef();
        }
        else if (iid == __uuidof(IAudioVolumeDuckNotification))
        {
            *ReturnValue = static_cast<IAudioVolumeDuckNotification *>(this);
            AddRef();
        }
        else
        {
            return E_NOINTERFACE;
        }
        return S_OK;
    }
    ULONG AddRef()
    {
        return InterlockedIncrement(&_Cref);
    }

    ULONG Release()
    {
        LONG ref = InterlockedDecrement(&_Cref);
        if (ref == 0)
        {
            delete this;
        }
        return 0;
    }
};

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>
 

 

