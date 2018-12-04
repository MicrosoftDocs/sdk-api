---
UID: NF:d3dcsx.ID3DX11FFT.AttachBuffersAndPrecompute
title: ID3DX11FFT::AttachBuffersAndPrecompute
author: windows-sdk-content
description: Attaches buffers to an FFT context and performs any required precomputations.
old-location: direct3d11\id3dx11fft_attachbuffersandprecompute.htm
tech.root: direct3d11
ms.assetid: 50c714fc-91fb-4a7d-a430-40ff221a1a14
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AttachBuffersAndPrecompute, AttachBuffersAndPrecompute method [Direct3D 11], AttachBuffersAndPrecompute method [Direct3D 11],ID3DX11FFT interface, ID3DX11FFT interface [Direct3D 11],AttachBuffersAndPrecompute method, ID3DX11FFT.AttachBuffersAndPrecompute, ID3DX11FFT::AttachBuffersAndPrecompute, d035d5bc-194b-3f37-2b54-5d5f4ae0fbc8, d3dcsx/ID3DX11FFT::AttachBuffersAndPrecompute, direct3d11.id3dx11fft_attachbuffersandprecompute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3dcsx.h
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11FFT.AttachBuffersAndPrecompute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT::AttachBuffersAndPrecompute


## -description


Attaches buffers to an FFT context and performs any required precomputations.


## -parameters




### -param NumTempBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers in <i>ppTempBuffers</i>.


### -param ppTempBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> pointers for the temporary buffers to attach. The FFT object might use these temporary buffers for its algorithm.


### -param NumPrecomputeBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers in <i>ppPrecomputeBuffers</i>.


### -param ppPrecomputeBufferSizes [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> pointers for the precompute buffers to attach. The FFT object might store precomputed data  in these buffers.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The <a href="https://msdn.microsoft.com/18db9e61-f1bc-4c70-8b2c-37305d9ac479">D3DX11_FFT_BUFFER_INFO</a> structure is initialized by a call to one of the create-FFT functions 
      (for example, <a href="https://msdn.microsoft.com/9a386221-b3ed-421d-aa98-933f7d267bdd">D3DX11CreateFFT</a>). For more create-FFT functions, see <a href="https://msdn.microsoft.com/426A132F-E398-473E-BD4E-3D1B4EC92E3F">D3DCSX 11 Functions</a>.

Use the info in <a href="https://msdn.microsoft.com/18db9e61-f1bc-4c70-8b2c-37305d9ac479">D3DX11_FFT_BUFFER_INFO</a> to allocate raw buffers of the specified (or larger) sizes and then call the <b>AttachBuffersAndPrecompute</b> to register the buffers with the FFT object.

Although you can share temporary buffers between multiple
      device contexts, we recommend not to concurrently execute multiple FFT objects that share temporary buffers.

Some FFT algorithms benefit from precomputing sin and cos. The FFT object might store precomputed data  in the user-supplied precompute buffers.




## -see-also




<a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>
 

 

