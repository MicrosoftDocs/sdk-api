---
UID: NF:d3d10.ID3D10Device.GSGetShaderResources
title: ID3D10Device::GSGetShaderResources
author: windows-sdk-content
description: Get the geometry shader resources.
old-location: direct3d10\id3d10device_gsgetshaderresources.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetshaderresources.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 1f730e36-30d4-870c-a3ab-3a6e91123778, GSGetShaderResources, GSGetShaderResources method [Direct3D 10], GSGetShaderResources method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetShaderResources method, ID3D10Device.GSGetShaderResources, ID3D10Device::GSGetShaderResources, d3d10/ID3D10Device::GSGetShaderResources, direct3d10.id3d10device_gsgetshaderresources
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
 - ID3D10Device.GSGetShaderResources
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GSGetShaderResources


## -description


Get the geometry shader resources.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin getting shader resources from.


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of resources to get from the device. Up to a maximum of 128 slots are available for shader resources.


### -param ppShaderResourceViews [out]

Type: <b><a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView</a>**</b>

Array of <a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">shader resource view</a> interfaces to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

