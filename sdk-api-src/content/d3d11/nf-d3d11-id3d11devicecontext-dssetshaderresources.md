---
UID: NF:d3d11.ID3D11DeviceContext.DSSetShaderResources
title: ID3D11DeviceContext::DSSetShaderResources
author: windows-sdk-content
description: Bind an array of shader resources to the domain-shader stage.
old-location: direct3d11\id3d11devicecontext_dssetshaderresources.htm
tech.root: direct3d11
ms.assetid: 633aedf7-f5cc-4873-940a-1b6e15927ec6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DSSetShaderResources, DSSetShaderResources method [Direct3D 11], DSSetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSSetShaderResources method, ID3D11DeviceContext.DSSetShaderResources, ID3D11DeviceContext::DSSetShaderResources, d3d11/ID3D11DeviceContext::DSSetShaderResources, direct3d11.id3d11devicecontext_dssetshaderresources, f29f7cbd-7143-217f-643c-21533afc6cda
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
 - ID3D11DeviceContext.DSSetShaderResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DSSetShaderResources


## -description


Bind an array of shader resources to the domain-shader stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources(ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).


### -param ppShaderResourceViews [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476628(v=VS.85).aspx">ID3D11ShaderResourceView</a>*</b>

Array of <a href="https://msdn.microsoft.com/en-us/library/Ff476628(v=VS.85).aspx">shader resource view</a> interfaces to set to the device.


## -returns



This method does not return a value.




## -remarks



If an overlapping resource view is already bound to an output slot, such as a render target, then the method will fill the destination shader resource slot with <b>NULL</b>.

For information about creating shader-resource views, see <a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">ID3D11Device::CreateShaderResourceView</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

