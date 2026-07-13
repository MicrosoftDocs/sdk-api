---
UID: NN:spatialaudioclient.ISpatialAudioClient2
tech.root: CoreAudio
title: ISpatialAudioClient2
ms.date: 01/31/2022
targetos: Windows
description: The **ISpatialAudioClient2** interface inherits from ISpatialAudioClient and adds methods to query for support for offloading large audio buffers.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: spatialaudioclient.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient2
f1_keywords:
 - ISpatialAudioClient2
 - spatialaudioclient/ISpatialAudioClient2
dev_langs:
 - c++
---

## -description

The **ISpatialAudioClient2** interface inherits from [ISpatialAudioClient](nn-spatialaudioclient-ispatialaudioclient) and adds methods to query for support for offloading large audio buffers.

## -remarks



Audio offloading allows an app to submit a large audio buffer (typically 1 to 2 seconds) to the audio device driver. Without offload, a typical audio buffer only contains 10ms of data, requiring the app to be awakened around 100 times per second to provide additional audio data. Using offloaded large buffers can provide battery savings, particularly for the scenario where the user is listening to audio with the screen off.

To use this feature, the driver for the audio device must support offloading. Query for support by calling [IsOffloadCapable](nf-spatialaudioclient-ispatialaudioclient2-isoffloadcapable). Determine the maximum number of audio frames supported for offloading by calling [GetMaxFrameCountForCategory](nf-spatialaudioclient-ispatialaudioclient2-getmaxframecountforcategory).

**ISpatialAudioClient2** was introduced in Windows 11 (Windows Build 22000), so your code should handle the case where it is running on an older version of Windows that doesn't include the interface. The following example illustrates using calling **QueryInterface** on **ISpatialAudioClient** to try to obtain an instance of **ISpatialAudioClient2** and checking that the retrieved interface is not null before calling its methods.

```cpp
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);

Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioClient2> spatialAudioClient2;
hr = spatialAudioClient->QueryInterface(__uuidof(ISpatialAudioClient2), (void**)&spatialAudioClient2);

if (spatialAudioClient2 != nullptr)
{
    BOOL offloadCapable = false;

    // AudioCategory_Media is just for example purposes.
    // Specify the same audio category that you intend specify in the call toISpatialAudioClient::ActivateSpatialAudioStream
    hr = spatialAudioClient2->IsOffloadCapable(AudioCategory_Media, &offloadCapable);
}
```

For UWP apps that do not have access to **IMMDevice**, you should get an instance of **ISpatialAudioClient** by calling <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>. For an example, see the [WindowsAudioSession sample](https://github.com/microsoft/Windows-universal-samples/tree/b1cb20f191d3fd99ce89df50c5b7d1a6e2382c01/Samples/WindowsAudioSession).

## -see-also

