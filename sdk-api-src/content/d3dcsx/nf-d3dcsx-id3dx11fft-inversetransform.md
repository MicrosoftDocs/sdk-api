---
UID: NF:d3dcsx.ID3DX11FFT.InverseTransform
title: ID3DX11FFT::InverseTransform (d3dcsx.h)
author: windows-sdk-content
description: Performs an inverse FFT.
old-location: direct3d11\id3dx11fft_inversetransform.htm
tech.root: direct3d11
ms.assetid: e4fe7a35-b039-4977-ba68-9869c5cc4383
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 9e07e88b-a097-403f-b882-754a12668d07, ID3DX11FFT interface [Direct3D 11],InverseTransform method, ID3DX11FFT.InverseTransform, ID3DX11FFT::InverseTransform, InverseTransform, InverseTransform method [Direct3D 11], InverseTransform method [Direct3D 11],ID3DX11FFT interface, d3dcsx/ID3DX11FFT::InverseTransform, direct3d11.id3dx11fft_inversetransform
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
 - ID3DX11FFT.InverseTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT::InverseTransform


## -description


Performs an inverse FFT.


## -parameters




### -param pInputBuffer [in]

Type: <b>const <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Pointer to <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> onto the input buffer.


### -param ppOutputBuffer [in, out]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> pointer.  If *<i>ppOutput</i> is <b>NULL</b>, then the computation will switch
          between temp buffers; in addition, the last buffer written to is stored at *<i>ppOutput</i>.
          Otherwise, *<i>ppOutput</i> is used as the output buffer (which might incur an extra copy).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>
 

 

