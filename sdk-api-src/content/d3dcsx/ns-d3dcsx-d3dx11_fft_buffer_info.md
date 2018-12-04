---
UID: NS:d3dcsx.D3DX11_FFT_BUFFER_INFO
title: D3DX11_FFT_BUFFER_INFO
author: windows-sdk-content
description: Describes buffer requirements for an FFT.
old-location: direct3d11\d3dx11_fft_buffer_info.htm
tech.root: direct3d11
ms.assetid: 18db9e61-f1bc-4c70-8b2c-37305d9ac479
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: D3DX11_FFT_BUFFER_INFO, D3DX11_FFT_BUFFER_INFO structure [Direct3D 11], d3dcsx/D3DX11_FFT_BUFFER_INFO, direct3d11.d3dx11_fft_buffer_info, f06d9ab2-6da1-c0ae-f9cc-c42662b380f5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dcsx.h
api_name:
 - D3DX11_FFT_BUFFER_INFO
product: Windows
targetos: Windows
req.typenames: D3DX11_FFT_BUFFER_INFO
req.redist: 
---

# D3DX11_FFT_BUFFER_INFO structure


## -description


Describes buffer requirements for an FFT.


## -struct-fields




### -field NumTempBufferSizes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of temporary buffers needed. 
            Allowed range is 0 to <b>D3DX11_FFT_MAX_TEMP_BUFFERS</b>.
          


### -field TempBufferFloatSizes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>[D3DX11_FFT_MAX_TEMP_BUFFERS]</b>

Minimum sizes (in FLOATs) of temporary buffers.
          


### -field NumPrecomputeBufferSizes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of precompute buffers required.  
            Allowed range is 0 to <b>D3DX11_FFT_MAX_PRECOMPUTE_BUFFERS</b>.
          


### -field PrecomputeBufferFloatSizes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>[D3DX11_FFT_MAX_PRECOMPUTE_BUFFERS]</b>

Minimum sizes (in FLOATs) for precompute buffers.
          


## -remarks



The <b>D3DX11_FFT_BUFFER_INFO</b> structure is initialized by a call to one of the create-FFT functions
          (for example, <a href="https://msdn.microsoft.com/9a386221-b3ed-421d-aa98-933f7d267bdd">D3DX11CreateFFT</a>).
          For more create-FFT functions, see <a href="https://msdn.microsoft.com/426A132F-E398-473E-BD4E-3D1B4EC92E3F">D3DCSX 11 Functions</a>.
        

Use the info in <b>D3DX11_FFT_BUFFER_INFO</b> to allocate raw buffers of the specified (or larger) sizes and then call the <a href="https://msdn.microsoft.com/50c714fc-91fb-4a7d-a430-40ff221a1a14">ID3DX11FFT::AttachBuffersAndPrecompute</a> method to register the buffers with the FFT object.
        

Some FFT algorithms benefit from precomputing sin and cos. The FFT object might store precomputed data in the user-supplied buffers.
        




## -see-also




<a href="https://msdn.microsoft.com/ED42B8D1-F4C9-489F-999B-A53BC96BA337">D3DCSX 11 Structures</a>
 

 

