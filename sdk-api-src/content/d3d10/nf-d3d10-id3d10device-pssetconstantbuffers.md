---
UID: NF:d3d10.ID3D10Device.PSSetConstantBuffers
title: ID3D10Device::PSSetConstantBuffers method
author: windows-driver-content
description: Set the constant buffers used by the pixel shader pipeline stage.
old-location: direct3d10\id3d10device_pssetconstantbuffers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetconstantbuffers.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D10Device, ID3D10Device interface [Direct3D 10], PSSetConstantBuffers method, ID3D10Device::PSSetConstantBuffers, PSSetConstantBuffers method [Direct3D 10], PSSetConstantBuffers method [Direct3D 10], ID3D10Device interface, PSSetConstantBuffers,ID3D10Device.PSSetConstantBuffers, d3d10/ID3D10Device::PSSetConstantBuffers, direct3d10.id3d10device_pssetconstantbuffers, e734dbaf-deb3-e52f-f92f-645994c1bd7d
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.PSSetConstantBuffers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::PSSetConstantBuffers method


## -description


Set the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting constant buffers to.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers to set.


### -param ppConstantBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>*</b>

Array of constant buffers (see <a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>) being given to the device.


## -returns



Returns nothing.




## -remarks



The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

