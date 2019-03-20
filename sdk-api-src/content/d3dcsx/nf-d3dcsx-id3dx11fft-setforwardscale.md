---
UID: NF:d3dcsx.ID3DX11FFT.SetForwardScale
title: ID3DX11FFT::SetForwardScale (d3dcsx.h)
author: windows-sdk-content
description: Sets the scale used for forward transforms.
old-location: direct3d11\id3dx11fft_setforwardscale.htm
tech.root: direct3d11
ms.assetid: afca03bb-459f-42ff-bc88-7487b1bc250d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3DX11FFT interface [Direct3D 11],SetForwardScale method, ID3DX11FFT.SetForwardScale, ID3DX11FFT::SetForwardScale, SetForwardScale, SetForwardScale method [Direct3D 11], SetForwardScale method [Direct3D 11],ID3DX11FFT interface, ceddf377-cf6d-2efb-3b7d-dcf4a17d5886, d3dcsx/ID3DX11FFT::SetForwardScale, direct3d11.id3dx11fft_setforwardscale
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
 - ID3DX11FFT.SetForwardScale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11FFT::SetForwardScale


## -description


Sets the scale used for forward transforms.


## -parameters




### -param ForwardScale [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

The scale to use for forward transforms.  Setting <i>ForwardScale</i> to 0 causes the default values of 1 to be used.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>SetForwardScale</b> sets the scale used by <a href="https://msdn.microsoft.com/da10b166-9561-4c04-b6b8-92b2daec30d7">ID3DX11FFT::ForwardTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>
 

 

