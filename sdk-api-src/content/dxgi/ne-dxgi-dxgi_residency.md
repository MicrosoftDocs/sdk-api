---
UID: NE:dxgi.DXGI_RESIDENCY
title: DXGI_RESIDENCY (dxgi.h)
description: Flags indicating the memory location of a resource.
helpviewer_keywords: ["DXGI_RESIDENCY","DXGI_RESIDENCY enumeration [DXGI]","DXGI_RESIDENCY_EVICTED_TO_DISK","DXGI_RESIDENCY_FULLY_RESIDENT","DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY","cfa66ca7-3d9d-67f6-1665-f4254ee73606","direct3ddxgi.DXGI_RESIDENCY","dxgi/DXGI_RESIDENCY","dxgi/DXGI_RESIDENCY_EVICTED_TO_DISK","dxgi/DXGI_RESIDENCY_FULLY_RESIDENT","dxgi/DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY"]
old-location: direct3ddxgi\DXGI_RESIDENCY.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_residency.htm
ms.date: 12/05/2018
ms.keywords: DXGI_RESIDENCY, DXGI_RESIDENCY enumeration [DXGI], DXGI_RESIDENCY_EVICTED_TO_DISK, DXGI_RESIDENCY_FULLY_RESIDENT, DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY, cfa66ca7-3d9d-67f6-1665-f4254ee73606, direct3ddxgi.DXGI_RESIDENCY, dxgi/DXGI_RESIDENCY, dxgi/DXGI_RESIDENCY_EVICTED_TO_DISK, dxgi/DXGI_RESIDENCY_FULLY_RESIDENT, dxgi/DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY
req.header: dxgi.h
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
req.typenames: DXGI_RESIDENCY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_RESIDENCY
 - dxgi/DXGI_RESIDENCY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_RESIDENCY
---

# DXGI_RESIDENCY enumeration


## -description

Flags indicating the memory location of a resource.

## -enum-fields

### -field DXGI_RESIDENCY_FULLY_RESIDENT:1

The resource is located in video memory.

### -field DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY:2

At least some of the resource is located in CPU memory.

### -field DXGI_RESIDENCY_EVICTED_TO_DISK:3

At least some of the resource has been paged out to the hard drive.

## -remarks

This enum is used by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-queryresourceresidency">QueryResourceResidency</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
