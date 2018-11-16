---
UID: NF:d3d11.ID3D11DeviceContext.HSGetShaderResources
title: ID3D11DeviceContext::HSGetShaderResources
author: windows-sdk-content
description: Get the hull-shader resources.
old-location: direct3d11\id3d11devicecontext_hsgetshaderresources.htm
tech.root: direct3d11
ms.assetid: 21956575-5f4b-48ca-944b-5cab57d02c7f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HSGetShaderResources, HSGetShaderResources method [Direct3D 11], HSGetShaderResources method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSGetShaderResources method, ID3D11DeviceContext.HSGetShaderResources, ID3D11DeviceContext::HSGetShaderResources, d3d11/ID3D11DeviceContext::HSGetShaderResources, da564466-b697-f908-c81d-dda7a85378db, direct3d11.id3d11devicecontext_hsgetshaderresources
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
 - ID3D11DeviceContext.HSGetShaderResources
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
- ID3D11DeviceContext.HSGetShaderResources
: 
---

# ID3D11DeviceContext::HSGetShaderResources


## -description


Get the hull-shader resources.


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
 

 

