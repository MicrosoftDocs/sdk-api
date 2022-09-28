---
UID: NN:mfidl.IMFCameraControlNotify
tech.root: mf
title: IMFCameraControlNotify
ms.date: 05/02/2022
targetos: Windows
description: Represents the notification callback for changes to camera controls. 
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraControlNotify
f1_keywords:
 - IMFCameraControlNotify
 - mfidl/IMFCameraControlNotify
dev_langs:
 - c++
helpviewer_keywords:
 - IMFCameraControlNotify
---

## -description

Represents the notification callback for changes to camera controls. 

## -remarks

Clients implement this interface to receive notifications when another app makes changes to the camera settings for a capture device. Pass the implementation into the [MFCreateCameraControlMonitor](nf-mfidl-mfcreatecameracontrolmonitor.md) function to create an instance of [IMFCameraControlMonitor](nn-mfidl-imfcameracontrolmonitor.md).

## -example

The following code examples demonstrate a typical implementation of this interface. For a complete example demonstrating the use of **IMFCameraControlNotify**, see the [ControlMonitorApp Sample](https://github.com/microsoft/Windows-Camera/tree/master/Samples/ControlMonitorApp/).

```cpp
//SampleClass.h
#pragma once

#include <mfapi.h>
#include <mfidl.h>
#include <string>
#include <iostream>
#include <wil/result.h>
#include <wil/com.h>

enum MONITOR_STATE
{
    MONITOR_UNINITIALIZED,
    MONITOR_STARTED,
    MONITOR_STOPPED,
    MONITOR_ERRORSTATE
};


class SampleClass :
    public IMFCameraControlNotify
{
public:
    static HRESULT CreateInstance(
        _In_ LPCWSTR symbolicName,
        _COM_Outptr_ SampleClass** sampleClass) noexcept;

    /// IUnknown
    IFACEMETHODIMP_(ULONG) AddRef(void) override;
    IFACEMETHODIMP_(ULONG) Release(void) override;
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Out_ LPVOID* ppvObject) override;

    /// IMFCameraControlNotify
    IFACEMETHODIMP_(void) OnChange(
        _In_ REFGUID controlSet,
        _In_ UINT32 controlId) override;
    IFACEMETHODIMP_(void) OnError(_In_ HRESULT hrStatus) override;
    HRESULT InitializeAndStart();
    HRESULT NotifyAny(bool enabled);
    void Shutdown();


    protected:
        SampleClass(LPCWSTR symbolicName) noexcept;
        virtual ~SampleClass() = default;
        HRESULT InternalInitialize();
    private:
        LONG m_lRef = 1;
        wil::critical_section m_lock;
        std::wstring m_symbolicName;
        wil::com_ptr_nothrow<IMFCameraControlMonitor> m_notificationMonitor;
        MONITOR_STATE m_monitorState = MONITOR_UNINITIALIZED;
        


};
```

```cpp
//SampleClass.cpp

#include "pch.h"
#include "SampleClass.h"

HRESULT SampleClass::CreateInstance(
    _In_ LPCWSTR symbolicName,
    _COM_Outptr_ SampleClass** sampleClass) noexcept try
{
    HRESULT hr = S_OK;
    wil::com_ptr_nothrow<SampleClass> sampleClassLocal;
    if (sampleClass == nullptr)
    {
        return E_POINTER;
    }
    *sampleClass = nullptr;
    sampleClassLocal.attach(new SampleClass(symbolicName));
    if (sampleClassLocal == nullptr)
    {
        return E_OUTOFMEMORY;
    }
    RETURN_IF_FAILED(sampleClassLocal.query_to(sampleClass));
    return hr;
} CATCH_RETURN();

SampleClass::SampleClass(LPCWSTR symbolicName) noexcept
    : m_symbolicName(symbolicName) 
{
}

void SampleClass::OnChange(_In_ REFGUID controlSet, _In_ UINT32 controlId) try
{
    std::cout << "Callback" << std::endl;
    // Example Scenario:

    // Checking if callback a known control in a custom ControlSet
    // Then retrieving current control value and update UI showing the camera’s control value
    // 
    // if ((controlSet == KSPROPERTYSETID_ANYCAMERACONTROL ||
    // controlSet == Custom_ControlSet) &&
    // controlId == Custom_ControlId)
    // {
    // GetControlStateAndUpdateUI(controlSet, controlId);
    // }} CATCH_LOG();
} CATCH_LOG();
        
void SampleClass::OnError(HRESULT hrStatus) try
{
    std::cout << "Unrecoverable error has occurred" << std::endl;
    auto lock = m_lock.lock();
    m_monitorState = MONITOR_ERRORSTATE;
} CATCH_LOG();
_Requires_lock_held_(m_lock)


HRESULT SampleClass::InternalInitialize()
{
    wil::com_ptr_nothrow<IMFCameraControlMonitor> localMonitor;
    if (m_notificationMonitor != nullptr)
    {
        (void)m_notificationMonitor->Shutdown();
        m_notificationMonitor = nullptr;
        m_monitorState = MONITOR_UNINITIALIZED;
    }
    RETURN_IF_FAILED(MFCreateCameraControlMonitor(
        m_symbolicName.c_str(),
        this,
        &localMonitor));
    RETURN_IF_FAILED(localMonitor->AddControlSubscription(
        PROPSETID_VIDCAP_VIDEOPROCAMP,
        KSPROPERTY_VIDEOPROCAMP_BRIGHTNESS));
    RETURN_IF_FAILED(localMonitor->AddControlSubscription(
        PROPSETID_VIDCAP_CAMERACONTROL,
        KSPROPERTY_CAMERACONTROL_EXPOSURE));
    RETURN_IF_FAILED(localMonitor->AddControlSubscription(
        KSPROPERTYSETID_ExtendedCameraControl,
        KSPROPERTY_CAMERACONTROL_EXTENDED_EVCOMPENSATION));
    RETURN_IF_FAILED(localMonitor->AddControlSubscription(
        KSPROPERTYSETID_ExtendedCameraControl,
        KSPROPERTY_CAMERACONTROL_EXTENDED_EXPOSUREMODE));
    m_notificationMonitor = localMonitor;
    m_monitorState = MONITOR_STOPPED;
    return S_OK;
}

HRESULT SampleClass::NotifyAny(bool enabled) 
{
    auto lock = m_lock.lock();
    if (m_monitorState == MONITOR_ERRORSTATE)
    {
        RETURN_IF_FAILED(InternalInitialize());
    }
    else
    {
        if (m_monitorState == MONITOR_STARTED)
        {
            HRESULT hr = m_notificationMonitor->Stop();
            if (FAILED(hr))
            {
                m_monitorState = MONITOR_ERRORSTATE;
                (void)m_notificationMonitor->Shutdown();
                RETURN_IF_FAILED(hr);
            }
            m_monitorState = MONITOR_STOPPED;
        }
        if (!enabled)
        {
            RETURN_IF_FAILED(m_notificationMonitor->RemoveControlSubscription(KSPROPERTYSETID_ANYCAMERACONTROL, 0));
        }
    }
    if (enabled)
    {
        RETURN_IF_FAILED(m_notificationMonitor->AddControlSubscription(KSPROPERTYSETID_ANYCAMERACONTROL, 0));
    }
    
    RETURN_IF_FAILED(m_notificationMonitor->Start());
    m_monitorState = MONITOR_STARTED;
    return S_OK;
}
void SampleClass::Shutdown()
{
    auto lock = m_lock.lock();
    if (m_notificationMonitor != nullptr)
    {
        m_notificationMonitor->Shutdown();
        m_notificationMonitor = nullptr;
    }
}
HRESULT SampleClass::InitializeAndStart()
{
    HRESULT hr = S_OK;
    auto lock = m_lock.lock();
    RETURN_IF_FAILED(InternalInitialize());
    hr = m_notificationMonitor->Start();
    if (FAILED(hr))
    {
        m_notificationMonitor = nullptr;
    }
    else
    {
        m_monitorState = MONITOR_STARTED;
    }

    return hr;
}


STDMETHODIMP_(ULONG) SampleClass::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) SampleClass::Release()
{
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }

    return uCount;
}

STDMETHODIMP SampleClass::QueryInterface(REFIID iid, void** ppv)
{
    RETURN_HR_IF_NULL(E_POINTER, ppv);

    if (iid == IID_IUnknown)
    {
        *ppv = static_cast<IUnknown*>(static_cast<IMFCameraControlNotify*>(this));
    }
    else if (iid == __uuidof(IMFCameraControlNotify))
    {
        *ppv = static_cast<IMFCameraControlNotify*>(this);
    }
    else
    {
        *ppv = NULL;
        return E_NOINTERFACE;
    }

    AddRef();

    return S_OK;
}
```


```cpp
// main.cpp
```

## -see-also

