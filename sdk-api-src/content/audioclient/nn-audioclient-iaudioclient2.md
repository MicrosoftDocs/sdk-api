---
UID: NN:audioclient.IAudioClient2
title: IAudioClient2
author: windows-sdk-content
description: The IAudioClient2 interface is derived from the IAudioClient interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following:\_opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.
old-location: coreaudio\iaudioclient2.htm
tech.root: CoreAudio
ms.assetid: 9CE79CEB-115E-4802-A687-B2CB23E6A0E0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioClient2, IAudioClient2 interface [Core Audio], IAudioClient2 interface [Core Audio],described, audioclient/IAudioClient2, coreaudio.iaudioclient2
ms.topic: interface
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - Audioclient.h
api_name:
 - IAudioClient2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioClient2 interface


## -description


The <b>IAudioClient2</b> interface is derived from the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following: opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.</p> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioClient2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioClient2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioClient2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCB6066E-2672-4E56-83EA-7EBEC3C7F3DD">GetBufferSizeLimits</a>
</td>
<td align="left" width="63%">
Retrieves the buffer size limits of the hardware audio engine in 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/275A6EB4-E6C7-4510-8EEA-BDBAFB1C06C3">IsOffloadCapable</a>
</td>
<td align="left" width="63%">
Retrieves information about whether or not the endpoint on which a stream is created is capable of supporting an offloaded stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">SetClientProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of the audio stream by populating an <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> structure.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a>



<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a>
 

 

