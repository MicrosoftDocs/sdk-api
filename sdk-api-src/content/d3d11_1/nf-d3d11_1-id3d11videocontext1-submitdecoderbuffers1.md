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

# ID3D11VideoContext1::SubmitDecoderBuffers1


## -description


Submits one or more buffers for decoding.


## -parameters




### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call the <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a> method.


### -param NumBuffers [in]

Type: <b>UINT</b>

The number of buffers submitted for decoding.


### -param pBufferDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/B35E4E27-6D69-49D4-908E-6EBF6DF5689A">D3D11_VIDEO_DECODER_BUFFER_DESC1</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/B35E4E27-6D69-49D4-908E-6EBF6DF5689A">D3D11_VIDEO_DECODER_BUFFER_DESC1</a> structures. The <i>NumBuffers</i> parameter specifies the number of elements in the array. Each element in the array describes a compressed buffer for decoding.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -remarks



This function does not honor any D3D11 predicate that may have been set.

<a href="https://msdn.microsoft.com/c8a2813e-56db-421b-ad37-d353c327a457">D3D11_QUERY_DATA_PIPELINE_STATISTICS</a> will not include this function for any feature level.





## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

