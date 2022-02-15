---
UID: NE:d3d12.D3D12_CPU_PAGE_PROPERTY
title: D3D12_CPU_PAGE_PROPERTY (d3d12.h)
description: Specifies the CPU-page properties for the heap.
helpviewer_keywords: ["D3D12_CPU_PAGE_PROPERTY","D3D12_CPU_PAGE_PROPERTY enumeration","D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE","D3D12_CPU_PAGE_PROPERTY_UNKNOWN","D3D12_CPU_PAGE_PROPERTY_WRITE_BACK","D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE","d3d12/D3D12_CPU_PAGE_PROPERTY","d3d12/D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE","d3d12/D3D12_CPU_PAGE_PROPERTY_UNKNOWN","d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_BACK","d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE","direct3d12.d3d12_cpu_page_property"]
old-location: direct3d12\d3d12_cpu_page_property.htm
tech.root: direct3d12
ms.assetid: 92C1DBB9-213C-4623-B6AA-B790E081F123
ms.date: 12/05/2018
ms.keywords: D3D12_CPU_PAGE_PROPERTY, D3D12_CPU_PAGE_PROPERTY enumeration, D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE, D3D12_CPU_PAGE_PROPERTY_UNKNOWN, D3D12_CPU_PAGE_PROPERTY_WRITE_BACK, D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE, d3d12/D3D12_CPU_PAGE_PROPERTY, d3d12/D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE, d3d12/D3D12_CPU_PAGE_PROPERTY_UNKNOWN, d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_BACK, d3d12/D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE, direct3d12.d3d12_cpu_page_property
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
targetos: Windows
req.typenames: D3D12_CPU_PAGE_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CPU_PAGE_PROPERTY
 - d3d12/D3D12_CPU_PAGE_PROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_CPU_PAGE_PROPERTY
---

# D3D12_CPU_PAGE_PROPERTY enumeration


## -description

Specifies the CPU-page properties for the heap.

## -enum-fields

### -field D3D12_CPU_PAGE_PROPERTY_UNKNOWN:0

The CPU-page property is unknown.

### -field D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE:1

The CPU cannot access the heap, therefore no page properties are available.

### -field D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE:2

The CPU-page property is write-combined.

### -field D3D12_CPU_PAGE_PROPERTY_WRITE_BACK:3

The CPU-page property is write-back.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
