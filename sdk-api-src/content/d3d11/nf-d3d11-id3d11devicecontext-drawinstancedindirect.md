---
UID: NF:d3d11.ID3D11DeviceContext.DrawInstancedIndirect
title: ID3D11DeviceContext::DrawInstancedIndirect
author: windows-sdk-content
description: Draw instanced, GPU-generated primitives.
old-location: direct3d11\id3d11devicecontext_drawinstancedindirect.htm
tech.root: direct3d11
ms.assetid: f40c662d-7cdc-4592-b8d5-72aad0b4dd53
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 2014c761-6e9c-961c-13a0-087ea9f94a6a, DrawInstancedIndirect, DrawInstancedIndirect method [Direct3D 11], DrawInstancedIndirect method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawInstancedIndirect method, ID3D11DeviceContext.DrawInstancedIndirect, ID3D11DeviceContext::DrawInstancedIndirect, d3d11/ID3D11DeviceContext::DrawInstancedIndirect, direct3d11.id3d11devicecontext_drawinstancedindirect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.DrawInstancedIndirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DrawInstancedIndirect


## -description


Draw instanced, GPU-generated primitives.


## -parameters




### -param pBufferForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>, which is a buffer containing the GPU generated primitives.


### -param AlignedByteOffsetForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Offset in <i>pBufferForArgs</i> to the start of the GPU generated primitives.


## -returns



Returns nothing.




## -remarks



When an application creates a buffer that is associated with the <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a> interface that  <i>pBufferForArgs</i> points to, the application must set the <a href="https://msdn.microsoft.com/en-us/library/Ff476203(v=VS.85).aspx">D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS</a> flag in the <b>MiscFlags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ff476092(v=VS.85).aspx">D3D11_BUFFER_DESC</a> structure that describes the buffer. To create the buffer, the application calls the <a href="https://msdn.microsoft.com/en-us/library/Ff476501(v=VS.85).aspx">ID3D11Device::CreateBuffer</a> method and in this call passes a pointer to <b>D3D11_BUFFER_DESC</b> in the <i>pDesc</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

