---
UID: NF:d3dcsx.D3DX11CreateFFT3DComplex
title: D3DX11CreateFFT3DComplex function
author: windows-sdk-content
description: Creates an ID3DX11FFT COM interface object.
old-location: direct3d11\d3dx11createfft3dcomplex.htm
old-project: direct3d11
ms.assetid: ca83d358-317a-4345-9509-c6c2b376f635
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 49defd9b-8123-3738-9c85-f49df8aa4076, D3DX11CreateFFT3DComplex, D3DX11CreateFFT3DComplex function [Direct3D 11], d3dcsx/D3DX11CreateFFT3DComplex, direct3d11.d3dx11createfft3dcomplex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3DX11_SCAN_OPCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateFFT3DComplex
product: Windows
targetos: Windows
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
---

# D3DX11CreateFFT3DComplex function


## -description


Creates an <a href="https://msdn.microsoft.com/6979aea4-5121-4a65-85f6-4b5753083715">ID3DX11FFT</a> COM interface object.


## -parameters




### -param pDeviceContext

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface to use for the FFT.


### -param X

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the first dimension of the FFT.


### -param Y

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the second dimension of the FFT.


### -param Z

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the third dimension of the FFT.


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
 

 

