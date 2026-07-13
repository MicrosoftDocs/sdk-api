---
UID: NN:spatialaudioclient.ISpatialAudioClient
title: ISpatialAudioClient (spatialaudioclient.h)
description: The ISpatialAudioClient interface enables a client to create audio streams that emit audio from a position in 3D space.
helpviewer_keywords: ["ISpatialAudioClient","ISpatialAudioClient interface [Core Audio]","ISpatialAudioClient interface [Core Audio]","described","coreaudio.ispatialaudioclient","spatialaudioclient/ISpatialAudioClient"]
old-location: coreaudio\ispatialaudioclient.htm
tech.root: CoreAudio
ms.assetid: 950778D4-79FE-4222-951F-5A456A633124
ms.date: 12/05/2018
ms.keywords: ISpatialAudioClient, ISpatialAudioClient interface [Core Audio], ISpatialAudioClient interface [Core Audio],described, coreaudio.ispatialaudioclient, spatialaudioclient/ISpatialAudioClient
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ISpatialAudioClient
 - spatialaudioclient/ISpatialAudioClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient
---

# ISpatialAudioClient interface


## -description

The <b>ISpatialAudioClient</b> interface enables a client to create audio streams that emit audio from a position in 3D space. This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioClient</b> also has these types of members:

## -remarks

The following example code illustrates how to initialize this interface using **IMMDevice**.


```cpp
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);

Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

```

For UWP apps that do not have access to **IMMDevice**, you should get an instance of **ISpatialAudioClient** by calling <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>. For an example, see the [WindowsAudioSession sample](https://github.com/microsoft/Windows-universal-samples/tree/b1cb20f191d3fd99ce89df50c5b7d1a6e2382c01/Samples/WindowsAudioSession).


<div class="alert"><b>Note</b>  When using the <b>ISpatialAudioClient</b> interfaces on an Xbox One Development Kit (XDK) title, you must first call <b>EnableSpatialAudio</b> before calling <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a> or <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>. Failure to do so will result in an E_NOINTERFACE error being returned from the call to Activate. <b>EnableSpatialAudio</b> is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</div>
<div> </div>
To access the <b>ActivateAudioIntefaceAsync</b>, you will need to link to mmdevapi.lib.
