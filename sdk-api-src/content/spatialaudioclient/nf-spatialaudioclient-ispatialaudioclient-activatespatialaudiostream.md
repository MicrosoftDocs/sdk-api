---
UID: NF:spatialaudioclient.ISpatialAudioClient.ActivateSpatialAudioStream
title: ISpatialAudioClient::ActivateSpatialAudioStream (spatialaudioclient.h)
author: windows-sdk-content
description: Activates and initializes spatial audio stream using one of the spatial audio stream activation structures.
old-location: coreaudio\ispatialaudioclient_activatespatialaudiostream.htm
tech.root: CoreAudio
ms.assetid: CBBB5A62-D342-4FB7-890C-9FE37949CC07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ActivateSpatialAudioStream, ActivateSpatialAudioStream method [Core Audio], ActivateSpatialAudioStream method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],ActivateSpatialAudioStream method, ISpatialAudioClient.ActivateSpatialAudioStream, ISpatialAudioClient::ActivateSpatialAudioStream, coreaudio.ispatialaudioclient_activatespatialaudiostream, spatialaudioclient/ISpatialAudioClient::ActivateSpatialAudioStream
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.ActivateSpatialAudioStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioClient::ActivateSpatialAudioStream


## -description


Activates and initializes spatial audio stream using one of the spatial audio stream activation structures.  



## -parameters




### -param activationParams [in]

The structure defining the activation parameters for the spatial audio stream. The <b>vt</b> field should be set to VT_BLOB and the <b>blob</b> field should be  populated with a <a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a> or a <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a>.


### -param riid [in]

The UUID of the spatial audio stream interface to activate.


### -param stream [out]

A pointer to the pointer which receives the activated spatial audio interface.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



This method supports activation of the following spatial audio stream interfaces:


<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a>



#### Examples


```cpp
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);

```





## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>



<a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a>



<a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a>
 

 

