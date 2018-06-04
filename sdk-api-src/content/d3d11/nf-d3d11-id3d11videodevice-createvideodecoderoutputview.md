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

# ID3D11VideoDevice::CreateVideoDecoderOutputView


## -description


Creates a resource view for a video decoder, describing the output sample for the decoding operation.


## -parameters




### -param pResource [in]

A pointer to the <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface of the decoder surface. The resource must be created with the <b>D3D11_BIND_DECODER</b> flag. See <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>.


### -param pDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/0A0C29C5-C3A3-43E7-86DA-1849AC276060">D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC</a> structure that describes the view.


### -param ppVDOVView [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/389E0CCC-4DD2-4E82-84D7-3794AEE59208">ID3D11VideoDecoderOutputView</a> interface. The caller must release the interface. If this parameter is <b>NULL</b>, the method checks whether the view is supported, but does not create the view. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Set the <i>ppVDOVView</i> parameter to <b>NULL</b> to test whether a view is supported.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

