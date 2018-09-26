---
UID: NE:d3d12.D3D12_BUFFER_UAV_FLAGS
title: D3D12_BUFFER_UAV_FLAGS
author: windows-sdk-content
description: Identifies unordered-access view options for a buffer resource.
old-location: direct3d12\d3d12_buffer_uav_flags.htm
tech.root: direct3d12
ms.assetid: D5350B5B-4E15-4B9F-B3E0-5A3B1592ED5C
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_BUFFER_UAV_FLAGS, D3D12_BUFFER_UAV_FLAGS enumeration, D3D12_BUFFER_UAV_FLAG_NONE, D3D12_BUFFER_UAV_FLAG_RAW, d3d12/D3D12_BUFFER_UAV_FLAGS, d3d12/D3D12_BUFFER_UAV_FLAG_NONE, d3d12/D3D12_BUFFER_UAV_FLAG_RAW, direct3d12.d3d12_buffer_uav_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_BUFFER_UAV_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_BUFFER_UAV_FLAGS
req.redist: 
---

# D3D12_BUFFER_UAV_FLAGS enumeration


## -description


Identifies unordered-access view options for a buffer resource.


## -enum-fields




### -field D3D12_BUFFER_UAV_FLAG_NONE

Indicates a default view.
          


### -field D3D12_BUFFER_UAV_FLAG_RAW

Resource contains raw, unstructured data.  Requires the UAV format to be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32_TYPELESS</a>.
            For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/9e991ab0-9648-484a-9a2c-5391ee5abf20">Raw Views of Buffers</a>.
          


## -remarks



This enum is used in the <a href="https://msdn.microsoft.com/13E48B8F-4EF7-45B7-88F2-61D9BA1801D2">D3D12_BUFFER_UAV</a>  structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

