---
UID: NF:d3dcsx.ID3DX11FFT.SetInverseScale
title: ID3DX11FFT::SetInverseScale
author: windows-sdk-content
description: Sets the scale used for inverse transforms.
old-location: direct3d11\id3dx11fft_setinversescale.htm
tech.root: direct3d11
ms.assetid: db29b6f8-ee36-48b6-8e28-f4bbaa6b0a7f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3DX11FFT interface [Direct3D 11],SetInverseScale method, ID3DX11FFT.SetInverseScale, ID3DX11FFT::SetInverseScale, SetInverseScale, SetInverseScale method [Direct3D 11], SetInverseScale method [Direct3D 11],ID3DX11FFT interface, d3dcsx/ID3DX11FFT::SetInverseScale, direct3d11.id3dx11fft_setinversescale, e2fd7d2b-bce2-191f-6387-e478c2a535fb
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
 - ID3DX11FFT.SetInverseScale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT::SetInverseScale


## -description


Sets the scale used for inverse transforms.


## -parameters




### -param InverseScale [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Scale used for inverse transforms.  Setting <i>InverseScale</i> to 0 causes the default value of 1/N to be used, 
          where N is the product of the transformed dimension lengths.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>SetInverseScale</b> sets the scale used by <a href="https://msdn.microsoft.com/e4fe7a35-b039-4977-ba68-9869c5cc4383">ID3DX11FFT::InverseTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>
 

 

