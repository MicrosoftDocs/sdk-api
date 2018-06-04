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

# ID3D11VideoContext::DecoderBeginFrame


## -description


Starts a decoding operation to decode a video frame.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param pView [in]

A pointer to the <a href="https://msdn.microsoft.com/389E0CCC-4DD2-4E82-84D7-3794AEE59208">ID3D11VideoDecoderOutputView</a> interface. This interface describes the resource that will receive the decoded frame. To get this pointer, call <a href="https://msdn.microsoft.com/8A3D72CF-B641-4219-8C88-FCE5231CF2F6">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>.


### -param ContentKeySize [in]

The size of the content key that is specified in <i>pContentKey</i>. If <i>pContentKey</i> is NULL, set <i>ContentKeySize</i> to zero.


### -param pContentKey [in]

An optional pointer to a content key that was used to encrypt the frame data. If no content key was used, set this parameter to <b>NULL</b>. If the caller provides a content key, the caller must use the session key to encrypt the content key.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.  <b>D3DERR_WASSTILLDRAWING</b> or <b>E_PENDING</b> is returned if the harware is busy, in which case the decoder should try to make the call again.




## -remarks



After this method is called, call <a href="https://msdn.microsoft.com/39010E57-FFF2-4793-B839-E336E8D2C1B2">ID3D11VideoContext::SubmitDecoderBuffers</a> to perform decoding operations. When all decoding operations have been executed, call <a href="https://msdn.microsoft.com/3596B70C-4BED-49C4-A0E4-8702DA219B01">ID3D11VideoContext::DecoderEndFrame</a>.



Each call to <b>DecoderBeginFrame</b> must have a matching call to <a href="https://msdn.microsoft.com/3596B70C-4BED-49C4-A0E4-8702DA219B01">DecoderEndFrame</a>. In most cases you cannot nest <b>DecoderBeginFrame</b> calls, but some codecs, such as  like VC-1, can have nested <b>DecoderBeginFrame</b> calls for special operations like post processing.

The following encryption scenarios are supported through the content key:

<ul>
<li>The decoder can choose to not encrypt every frame, for example  it may only encrypt the I frames and not encrypt the P/B frames.  In these scenario, the decoder will specify pContentKey = NULL and ContentKeySize = 0 for those frames that it does not encrypt.</li>
<li>The decoder can choose to encrypt the compressed buffers using the session key.  In this scenario, the decoder will specify a content key containing all zeros.</li>
<li>The decoder can choose to encrypt the compressed buffers using a separate content key.  In this scenario, the decoder will ECB encrypt the content key using the session key and pass the encrypted content key.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

