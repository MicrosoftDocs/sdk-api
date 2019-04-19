---
UID: NN:audioengineendpoint.IAudioEndpointLastBufferControl
title: IAudioEndpointLastBufferControl (audioengineendpoint.h)
author: windows-sdk-content
description: Provides functionality to allow an offload stream client to notify the endpoint that the last buffer has been sent only partially filled.
old-location: coreaudio\iaudioendpointlastbuffercontrol.htm
tech.root: CoreAudio
ms.assetid: 79f4b370-fd04-41a9-ad74-54f7edd084c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointLastBufferControl, IAudioEndpointLastBufferControl interface [Core Audio], IAudioEndpointLastBufferControl interface [Core Audio],described, audioengineendpoint/IAudioEndpointLastBufferControl, coreaudio.iaudioendpointlastbuffercontrol
ms.topic: interface
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AudioEngineEndpoint.idl
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
 - audioengineendpoint.h
api_name:
 - IAudioEndpointLastBufferControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointLastBufferControl interface


## -description


Provides functionality to allow an offload stream client to notify  the endpoint that the last buffer has been sent only partially filled.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointLastBufferControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointLastBufferControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointLastBufferControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ee7095a-957f-429d-b19d-df90246f8608">IsLastBufferControlSupported</a>
</td>
<td align="left" width="63%">
Indicates if last buffer control is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ff0232d-acf6-44e7-933a-b5ac91c3acc8">ReleaseOutputDataPointerForLastBuffer</a>
</td>
<td align="left" width="63%">
Releases the output data pointer for the last buffer.

</td>
</tr>
</table> 


## -remarks



This is an optional interface on an endpoint.




## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

