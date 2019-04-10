---
UID: NF:d3dcsx.D3DX11CreateFFT1DReal
title: D3DX11CreateFFT1DReal function (d3dcsx.h)
author: windows-sdk-content
description: Creates an ID3DX11FFT COM interface object.
old-location: direct3d11\d3dx11createfft1dreal.htm
tech.root: direct3d11
ms.assetid: 49186642-2591-4943-b686-83bf24f470dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 542c01f8-d563-c1ab-aa89-495a7e96e411, D3DX11CreateFFT1DReal, D3DX11CreateFFT1DReal function [Direct3D 11], d3dcsx/D3DX11CreateFFT1DReal, direct3d11.d3dx11createfft1dreal
ms.topic: function
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
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateFFT1DReal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DX11CreateFFT1DReal function


## -description


Creates an <a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a> COM interface object.


## -parameters




### -param pDeviceContext

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface to use for the FFT.


### -param X

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the first dimension of the FFT.


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that affect the behavior of the FFT, can be 0 or a combination of flags from <a href="https://msdn.microsoft.com/0e7eab8d-bbc5-4704-aa92-35de4a1eda28">D3DX11_FFT_CREATE_FLAG</a>.


### -param pBufferInfo [out]

Type: <b><a href="https://msdn.microsoft.com/18db9e61-f1bc-4c70-8b2c-37305d9ac479">D3DX11_FFT_BUFFER_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/18db9e61-f1bc-4c70-8b2c-37305d9ac479">D3DX11_FFT_BUFFER_INFO</a> structure that receives the buffer requirements to execute the FFT algorithms. Use this info to allocate raw buffers of the specified (or larger) sizes and then call the <a href="https://msdn.microsoft.com/50c714fc-91fb-4a7d-a430-40ff221a1a14">ID3DX11FFT::AttachBuffersAndPrecompute</a> method to register the buffers with the FFT object.


### -param ppFFT [out]

Type: <b><a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a> interface for the created FFT object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

The return value is one of the values listed in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/426A132F-E398-473E-BD4E-3D1B4EC92E3F">D3DCSX 11 Functions</a>
 

 

