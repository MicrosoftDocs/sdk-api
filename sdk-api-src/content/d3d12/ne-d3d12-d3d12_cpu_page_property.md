---
UID: NE:d3d12.D3D12_CPU_PAGE_PROPERTY
title: D3D12_CPU_PAGE_PROPERTY (d3d12.h)
author: windows-sdk-content
description: Specifies the CPU-page properties for the heap.
old-location: direct3d12\d3d12_cpu_page_property.htm
tech.root: direct3d12
ms.assetid: 92C1DBB9-213C-4623-B6AA-B790E081F123
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_CPU_PAGE_PROPERTY, D3D12_CPU_PAGE_PROPERTY enumeration, D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE, D3D12_CPU_PAGE_PROPERTY_UNKNOWN, D3D12_CPU_PAGE_PROPERTY_WRITE_BACK, D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE, d3d12/D3D12_CPU_PAGE_PROPERTY, d3d12/D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE, d3d12/D3D12_CPU_PAGE_PROPERTY_UNKNOWN, d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_BACK, d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE, direct3d12.d3d12_cpu_page_property
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
 - D3D12_CPU_PAGE_PROPERTY
product: Windows
targetos: Windows
req.typenames: D3D12_CPU_PAGE_PROPERTY
req.redist: 
---

# D3D12_CPU_PAGE_PROPERTY enumeration


## -description


Specifies the CPU-page properties for the heap.


## -enum-fields




### -field D3D12_CPU_PAGE_PROPERTY_UNKNOWN

The CPU-page property is unknown.


### -field D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE

The CPU cannot access the heap, therefore no page properties are available.
          


### -field D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE

The CPU-page property is write-combined.


### -field D3D12_CPU_PAGE_PROPERTY_WRITE_BACK

The CPU-page property is write-back.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

