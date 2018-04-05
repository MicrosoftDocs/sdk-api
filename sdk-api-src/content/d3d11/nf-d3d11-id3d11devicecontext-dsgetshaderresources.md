---
UID: NF:d3d11.ID3D11DeviceContext.DSGetShaderResources
title: ID3D11DeviceContext::DSGetShaderResources method
author: windows-driver-content
description: Get the domain-shader resources.
old-location: direct3d11\id3d11devicecontext_dsgetshaderresources.htm
old-project: direct3d11
ms.assetid: 6308e37c-a30f-4927-946b-33d882f9cce8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 3f3f8f89-3e09-81e0-f528-c36e15994027, DSGetShaderResources method [Direct3D 11], DSGetShaderResources method [Direct3D 11], ID3D11DeviceContext interface, DSGetShaderResources,ID3D11DeviceContext.DSGetShaderResources, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], DSGetShaderResources method, ID3D11DeviceContext::DSGetShaderResources, d3d11/ID3D11DeviceContext::DSGetShaderResources, direct3d11.id3d11devicecontext_dsgetshaderresources
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
-	ID3D11DeviceContext.DSGetShaderResources
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::DSGetShaderResources method


## -description


Get the domain-shader resources.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - 1).


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources (ranges from 0 to D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT - StartSlot).


### -param ppShaderResourceViews [out, optional]

Type: <b><a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>**</b>

Array of <a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">shader resource view</a> interfaces to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

