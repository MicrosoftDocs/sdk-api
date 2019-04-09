---
UID: NF:d3d10.ID3D10Device.GSGetConstantBuffers
title: ID3D10Device::GSGetConstantBuffers (d3d10.h)
author: windows-sdk-content
description: Get the constant buffers used by the geometry shader pipeline stage.
old-location: direct3d10\id3d10device_gsgetconstantbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetconstantbuffers.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 31eb9c1b-cc8e-64bc-4567-a82debaa5287, GSGetConstantBuffers, GSGetConstantBuffers method [Direct3D 10], GSGetConstantBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetConstantBuffers method, ID3D10Device.GSGetConstantBuffers, ID3D10Device::GSGetConstantBuffers, d3d10/ID3D10Device::GSGetConstantBuffers, direct3d10.id3d10device_gsgetconstantbuffers
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
 - ID3D10Device.GSGetConstantBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::GSGetConstantBuffers


## -description


Get the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">geometry shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers to retrieve.


### -param ppConstantBuffers [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

