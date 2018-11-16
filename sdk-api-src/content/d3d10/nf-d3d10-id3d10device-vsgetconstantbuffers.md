---
UID: NF:d3d10.ID3D10Device.VSGetConstantBuffers
title: ID3D10Device::VSGetConstantBuffers
author: windows-sdk-content
description: Get the constant buffers used by the vertex shader pipeline stage.
old-location: direct3d10\id3d10device_vsgetconstantbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vsgetconstantbuffers.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 2359bc62-0205-acb7-f462-1ceafd1f8b80, ID3D10Device interface [Direct3D 10],VSGetConstantBuffers method, ID3D10Device.VSGetConstantBuffers, ID3D10Device::VSGetConstantBuffers, VSGetConstantBuffers, VSGetConstantBuffers method [Direct3D 10], VSGetConstantBuffers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSGetConstantBuffers, direct3d10.id3d10device_vsgetconstantbuffers
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.VSGetConstantBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.VSGetConstantBuffers
: 
---

# ID3D10Device::VSGetConstantBuffers


## -description


Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">constant buffers</a> used by the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers to retrieve.


### -param ppConstantBuffers [out]

Type: <b><a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

