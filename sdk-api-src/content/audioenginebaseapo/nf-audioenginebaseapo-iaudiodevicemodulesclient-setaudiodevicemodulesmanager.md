---
UID: NF:audioenginebaseapo.IAudioDeviceModulesClient.SetAudioDeviceModulesManager
tech.root: audio
title: IAudioDeviceModulesClient::SetAudioDeviceModulesManager
ms.date: 04/30/2021
targetos: Windows
description: Called by the system to pass an instance of **IAudioDeviceModulesManager** to Audio Processing Objects (APOs) that implement the **IAudioDeviceModulesClient** interface.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioenginebaseapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioDeviceModulesClient::SetAudioDeviceModulesManager
f1_keywords:
 - IAudioDeviceModulesClient::SetAudioDeviceModulesManager
 - audioenginebaseapo/IAudioDeviceModulesClient::SetAudioDeviceModulesManager
dev_langs:
 - c++
---

## -description

Called by the system to pass an instance of [AudioDeviceModulesManager](/uwp/api/windows.media.devices.audiodevicemodulesmanager) to Audio Processing Objects (APOs) that implement the [IAudioDeviceModulesClient](nn-audioenginebaseapo-iaudiodevicemodulesclient.md) interface.

## -parameters

### -param pAudioDeviceModulesManager

An **IUnknown** interface representing the **IAudioDeviceModulesManager**.

## -returns

An HRESULT.

## -remarks

The following code example illustrates an implementation of **IAudioDeviceModulesClient**.

```cpp
STDMETHODIMP CTestModuleAPO::SetAudioDeviceModulesManager(_In_ IUnknown* pAudioDeviceModulesManager) 
{
    HRESULT hr = S_OK;
    CComQIPtr<Windows::Media::Devices::IAudioDeviceModulesManager> spModuleManager = pAudioDeviceModulesManager;
    ComPtr<IVectorView<AudioDeviceModule *>> spModules;

    // Cache the audio modules manager for later use within the apo
    m_AudioModulesManager = pAudioDeviceModulesManager;

    // Search the audio modules for a known module
    hr = m_pAudioDeviceModulesMgr->FindAllById(KNOWN_MODULE_ID, &spModules);

    if (SUCCEEDED(hr))
    {
        // do something with the module(s) returned or cache them for later usage
        m_KnownModules = spModules;
    }

    return hr;
}

```

## -see-also

