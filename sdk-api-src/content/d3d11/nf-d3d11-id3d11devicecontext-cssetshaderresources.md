---
UID: NF:d3d11.ID3D11DeviceContext.CSSetShaderResources
title: ID3D11DeviceContext::CSSetShaderResources method
author: windows-driver-content
description: Bind an array of shader resources to the compute-shader stage.
old-location: direct3d11\id3d11devicecontext_cssetshaderresources.htm
old-project: direct3d11
ms.assetid: 04babe17-b053-49f4-90bc-8080f521079e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CSSetShaderResources method [Direct3D 11], CSSetShaderResources method [Direct3D 11], ID3D11DeviceContext interface, CSSetShaderResources,ID3D11DeviceContext.CSSetShaderResources, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], CSSetShaderResources method, ID3D11DeviceContext::CSSetShaderResources, cef14155-2203-ea99-84d2-f1722c5ae802, d3d11/ID3D11DeviceContext::CSSetShaderResources, direct3d11.id3d11devicecontext_cssetshaderresources
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.CSSetShaderResources
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::CSSetShaderResources method


## -description


Bind an array of shader resources to the compute-shader stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources(ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).


### -param ppShaderResourceViews [in, optional]

Type: <b><a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>*</b>

Array of <a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">shader resource view</a> interfaces to set to the device.


## -returns



This method does not return a value.




## -remarks



If an overlapping resource view is already bound to an output slot, such as a render target, then the method will fill the destination shader resource slot with <b>NULL</b>.

For information about creating shader-resource views, see <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>.


  The method will hold a reference to the interfaces passed in.
  This differs from the device state behavior in Direct3D 10.





## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

