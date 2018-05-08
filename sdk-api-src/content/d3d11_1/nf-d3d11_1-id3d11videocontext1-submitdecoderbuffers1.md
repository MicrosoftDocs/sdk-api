---
UID: NF:d3d11_1.ID3D11VideoContext1.SubmitDecoderBuffers1
title: ID3D11VideoContext1::SubmitDecoderBuffers1
author: windows-driver-content
description: Submits one or more buffers for decoding.
old-location: mf\id3d11videocontext1_submitdecoderbuffers1.htm
old-project: medfound
ms.assetid: 9E5FC926-71D7-4102-8952-EC0585B4A4FC
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],SubmitDecoderBuffers1 method, ID3D11VideoContext1.SubmitDecoderBuffers1, ID3D11VideoContext1::SubmitDecoderBuffers1, SubmitDecoderBuffers1, SubmitDecoderBuffers1 method [Media Foundation], SubmitDecoderBuffers1 method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::SubmitDecoderBuffers1, mf.id3d11videocontext1_submitdecoderbuffers1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_1.h
api_name:
-	ID3D11VideoContext1.SubmitDecoderBuffers1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

