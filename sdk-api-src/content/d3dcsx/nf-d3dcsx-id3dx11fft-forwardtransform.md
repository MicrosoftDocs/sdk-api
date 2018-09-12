---
UID: NF:d3dcsx.ID3DX11FFT.ForwardTransform
title: ID3DX11FFT::ForwardTransform
author: windows-sdk-content
description: Performs a forward FFT.
old-location: direct3d11\id3dx11fft_forwardtransform.htm
tech.root: direct3d11
ms.assetid: da10b166-9561-4c04-b6b8-92b2daec30d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ForwardTransform, ForwardTransform method [Direct3D 11], ForwardTransform method [Direct3D 11],ID3DX11FFT interface, ID3DX11FFT interface [Direct3D 11],ForwardTransform method, ID3DX11FFT.ForwardTransform, ID3DX11FFT::ForwardTransform, d3dcsx/ID3DX11FFT::ForwardTransform, direct3d11.id3dx11fft_forwardtransform, fbd555b1-86f3-8e92-7c5e-ed1c088e2207
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
 - ID3DX11FFT.ForwardTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT::ForwardTransform


## -description


Performs a forward FFT.


## -parameters




### -param pInputBuffer [in]

Type: <b>const <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Pointer to <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> onto the input buffer.


### -param ppOutputBuffer [in, out]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> pointer.  If *<i>ppOutputBuffer</i> is <b>NULL</b>, the computation will switch
          between temp buffers; in addition, the last buffer written to is stored at *<i>ppOutputBuffer</i>.
          Otherwise, *<i>ppOutputBuffer</i> is used as the output buffer (which might incur an extra copy).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>ForwardTransform</b> can be called after buffers have been attached to the context using <a href="https://msdn.microsoft.com/50c714fc-91fb-4a7d-a430-40ff221a1a14">ID3DX11FFT::AttachBuffersAndPrecompute</a>. The combination of <i>pInputBuffer</i> and *<i>ppOuputBuffer</i> can be one of the temp buffers.

The format of complex data is interleaved components (for example, (Real0, Imag0), 
      (Real1, Imag1) ... , and so on). Data is stored in row major order.




## -see-also




<a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>
 

 

