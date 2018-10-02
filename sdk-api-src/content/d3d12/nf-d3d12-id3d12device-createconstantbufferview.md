---
UID: NF:d3d12.ID3D12Device.CreateConstantBufferView
title: ID3D12Device::CreateConstantBufferView
author: windows-sdk-content
description: Creates a constant-buffer view for accessing resource data.
old-location: direct3d12\id3d12device_createconstantbufferview.htm
tech.root: direct3d12
ms.assetid: 13251F82-4AE9-4234-A0C8-0E666F8A1856
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CreateConstantBufferView, CreateConstantBufferView method, CreateConstantBufferView method,ID3D12Device interface, ID3D12Device interface,CreateConstantBufferView method, ID3D12Device.CreateConstantBufferView, ID3D12Device::CreateConstantBufferView, d3d12/ID3D12Device::CreateConstantBufferView, direct3d12.id3d12device_createconstantbufferview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateConstantBufferView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateConstantBufferView


## -description


Creates a constant-buffer view for accessing resource data.


## -parameters




### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/83A4522E-AE87-42CE-9B95-CF63E92556AD">D3D12_CONSTANT_BUFFER_VIEW_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/83A4522E-AE87-42CE-9B95-CF63E92556AD">D3D12_CONSTANT_BUFFER_VIEW_DESC</a> structure that describes the constant-buffer view.
          


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the constant-buffer view.
          


## -returns



Returns nothing.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

