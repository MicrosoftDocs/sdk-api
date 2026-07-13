---
UID: NF:audioclient.IAudioViewManagerService.SetAudioStreamWindow
tech.root: CoreAudio
title: IAudioViewManagerService::SetAudioStreamWindow
ms.date: 03/31/2022
targetos: Windows
description: Associates the specified HWND window handle with an audio stream.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioclient.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22621
req.target-min-winversvr: Windows Server, version 23H2
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioViewManagerService::SetAudioStreamWindow
f1_keywords:
 - IAudioViewManagerService::SetAudioStreamWindow
 - audioclient/IAudioViewManagerService::SetAudioStreamWindow
dev_langs:
 - c++
helpviewer_keywords:
 - SetAudioStreamWindow
---

## -description

Associates the specified [HWND](https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types) window handle with an audio stream.

## -parameters

### -param hwnd

The [HWND](https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types) with which the audio stream wll be associated.

## -returns

## -remarks

An app can choose to associate audio streams with a particular window of their app for proper audio location representation in a Mixed Reality scenario

Get an instance of the [IAudioViewManagerService](nn-audioclient-iaudioviewmanagerservice.md) by calling [GetService](nf-audioclient-iaudioclient-getservice.md) on the [IAudioClient](nn-audioclient-iaudioclient.md) instance representing the stream you want to associate a window with. The following code example illustrates creating an audio stream on the default audio render endpoint and associating it with an **HWND**.

```cpp
#include <audioclient.h>

HRESULT CreateAudioStreamAndAttachToHwnd(_In_ HWND hwnd, _Out_ IAudioClient **audioStream)
{

    wil::com_ptr_nothrow<IMMDeviceEnumerator> enumerator;
    RETURN_IF_FAILED(CoCreateInstance(__uuidof(IMMDeviceEnumerator),
    NULL,
    CLSCTX_ALL,
    IID_PPV_ARGS(&enumerator)));
    
    wil::com_ptr_nothrow<IMMDevice> device;
    RETURN_IF_FAILED(enumerator->GetDefaultAudioEndpoint(eRender, eConsole, &device));
    
    wil::com_ptr_nothrow<IAudioClient> audioClient;
    RETURN_IF_FAILED(device->Activate(__uuidof(IAudioClient),
    CLSCTX_ALL,
    NULL,
    (void**)&audioClient));
    
    wil::unique_cotaskmem_ptr<WAVEFORMATEX> wfx;
    RETURN_IF_FAILED(audioClient->GetMixFormat(wil::out_param_ptr<WAVEFORMATEX**>(wfx)));
    
    constexpr REFERENCE_TIME hnsRequestedDuration = 10000000;
    RETURN_IF_FAILED(audioClient->Initialize(AUDCLNT_SHAREMODE_SHARED,
    0,
    hnsRequestedDuration,
    0,
    wfx.get(),
    NULL));
    
    wil::com_ptr_nothrow<IAudioViewManagerService> audioViewManagerService;
    RETURN_IF_FAILED(audioClient->GetService(IID_PPV_ARGS(&audioViewManagerService)));
    RETURN_IF_FAILED(audioViewManagerService->SetAudioStreamWindow(hwnd));
    
    *audioStream = spAudioClient.detach();
    
    return S_OK;
}
```

## -see-also

