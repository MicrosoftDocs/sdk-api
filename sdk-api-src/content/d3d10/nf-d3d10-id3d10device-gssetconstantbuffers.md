---
UID: NF:d3d10.ID3D10Device.GSSetConstantBuffers
title: ID3D10Device::GSSetConstantBuffers
author: windows-sdk-content
description: Set the constant buffers used by the geometry shader pipeline stage.
old-location: direct3d10\id3d10device_gssetconstantbuffers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gssetconstantbuffers.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 4a93383e-8523-3db8-9e49-217d1cf3ff2b, GSSetConstantBuffers, GSSetConstantBuffers method [Direct3D 10], GSSetConstantBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSSetConstantBuffers method, ID3D10Device.GSSetConstantBuffers, ID3D10Device::GSSetConstantBuffers, d3d10/ID3D10Device::GSSetConstantBuffers, direct3d10.id3d10device_gssetconstantbuffers
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GSSetConstantBuffers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GSSetConstantBuffers


## -description


Set the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry shader</a> pipeline stage.


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



The method will not hold references to the interfaces passed in. For that reason, applications should be careful not to release interfaces currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

