---
UID: NF:d3d11.ID3D11DeviceContext.PSSetShaderResources
title: ID3D11DeviceContext::PSSetShaderResources
author: windows-sdk-content
description: Bind an array of shader resources to the pixel shader stage.
old-location: direct3d11\id3d11devicecontext_pssetshaderresources.htm
tech.root: direct3d11
ms.assetid: acccbde4-68d0-4c76-bf77-643884af1bbe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 321c7b79-1c69-8b42-8a25-c6a5965c84d5, ID3D11DeviceContext interface [Direct3D 11],PSSetShaderResources method, ID3D11DeviceContext.PSSetShaderResources, ID3D11DeviceContext::PSSetShaderResources, PSSetShaderResources, PSSetShaderResources method [Direct3D 11], PSSetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSSetShaderResources, direct3d11.id3d11devicecontext_pssetshaderresources
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
 - ID3D11DeviceContext.PSSetShaderResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.PSSetShaderResources
: 
---

# ID3D11DeviceContext::PSSetShaderResources


## -description


Bind an array of shader resources to the pixel shader stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).


### -param ppShaderResourceViews [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476628(v=VS.85).aspx">ID3D11ShaderResourceView</a>*</b>

Array of <a href="https://msdn.microsoft.com/en-us/library/Ff476628(v=VS.85).aspx">shader resource view</a> interfaces to set to the device.


## -returns



Returns nothing.




## -remarks



If an overlapping resource view is already bound to an output slot, such as a rendertarget, then this API will fill the destination shader resource slot with <b>NULL</b>.

For information about creating shader-resource views, see <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

