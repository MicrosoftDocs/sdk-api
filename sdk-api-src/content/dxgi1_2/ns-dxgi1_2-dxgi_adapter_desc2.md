---
UID: NS:dxgi1_2.DXGI_ADAPTER_DESC2
title: DXGI_ADAPTER_DESC2 (dxgi1_2.h)
description: Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.2.
helpviewer_keywords: ["DXGI_ADAPTER_DESC2","DXGI_ADAPTER_DESC2 structure [DXGI]","direct3ddxgi.dxgi_adapter_desc2","dxgi1_2/DXGI_ADAPTER_DESC2"]
old-location: direct3ddxgi\dxgi_adapter_desc2.htm
tech.root: direct3ddxgi
ms.assetid: AE34913A-84D8-49DB-A736-15AECA9989F9
ms.date: 12/05/2018
ms.keywords: DXGI_ADAPTER_DESC2, DXGI_ADAPTER_DESC2 structure [DXGI], direct3ddxgi.dxgi_adapter_desc2, dxgi1_2/DXGI_ADAPTER_DESC2
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_ADAPTER_DESC2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_ADAPTER_DESC2
 - dxgi1_2/DXGI_ADAPTER_DESC2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_ADAPTER_DESC2
---

# DXGI_ADAPTER_DESC2 structure


## -description

Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.2.

## -struct-fields

### -field Description

A string that contains the adapter description.

### -field VendorId

The PCI ID or ACPI ID of the adapter's hardware vendor. If this value is less than or equal to 0xFFFF, it is a PCI ID; otherwise, it is an ACPI ID.

### -field DeviceId

The PCI ID or ACPI ID of the adapter's hardware device. If <b>VendorId</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID.

### -field SubSysId

The PCI ID or ACPI ID of the adapter's hardware subsystem. If <b>VendorId</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID.

### -field Revision

The adapter's PCI or ACPI revision number. If <b>VendorId</b> is a PCI ID, it is a PCI device revision number; otherwise, it is an ACPI device revision number.

### -field DedicatedVideoMemory

The number of bytes of dedicated video memory that are not shared with the CPU.

### -field DedicatedSystemMemory

The number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.

### -field SharedSystemMemory

The number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.

### -field AdapterLuid

A unique value that identifies the adapter. See <a href="/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.

### -field Flags

A value of the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag">DXGI_ADAPTER_FLAG</a> enumerated type that describes the adapter type.  The <b>DXGI_ADAPTER_FLAG_REMOTE</b> flag is reserved.

### -field GraphicsPreemptionGranularity

A value of the <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity">DXGI_GRAPHICS_PREEMPTION_GRANULARITY</a> enumerated type that describes the granularity level at which the GPU can be preempted from performing its current graphics rendering task.

### -field ComputePreemptionGranularity

A value of the <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity">DXGI_COMPUTE_PREEMPTION_GRANULARITY</a> enumerated type that describes the granularity level at which the GPU can be preempted from performing its current compute task.

## -remarks

The <b>DXGI_ADAPTER_DESC2</b> structure provides a DXGI 1.2 description of an adapter.  This structure is initialized by using the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">IDXGIAdapter2::GetDesc2</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">IDXGIAdapter2::GetDesc2</a>