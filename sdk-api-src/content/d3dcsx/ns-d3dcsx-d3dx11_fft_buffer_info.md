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
 

 

