---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Microsoft::WRL::ComPtr&lt;ISpatialAudioClient&gt; spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice-&gt;Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&amp;spatialAudioClient);

hr = spatialAudioClient-&gt;IsAudioObjectFormatSupported(&amp;format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &amp;format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&amp;activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast&lt;BYTE *&gt;(&amp;streamParams);

Microsoft::WRL::ComPtr&lt;ISpatialAudioObjectRenderStream&gt; spatialAudioStream;
hr = spatialAudioClient-&gt;ActivateSpatialAudioStream(&amp;activationParams, __uuidof(spatialAudioStream), (void**)&amp;spatialAudioStream);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>



<a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a>



<a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a>
 

 

