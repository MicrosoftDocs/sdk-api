---
UID: NS:dxgi.DXGI_ADAPTER_DESC1
title: DXGI_ADAPTER_DESC1 (dxgi.h)
description: Describes an adapter (or video card) using DXGI 1.1.
helpviewer_keywords: ["44e46590-c7af-e371-28b4-890028cf955b","DXGI_ADAPTER_DESC1","DXGI_ADAPTER_DESC1 structure [DXGI]","direct3ddxgi.dxgi_adapter_desc1","dxgi/DXGI_ADAPTER_DESC1"]
old-location: direct3ddxgi\dxgi_adapter_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 0ae3bdb1-b122-439a-8f62-c831a9dd87e2
ms.date: 12/05/2018
ms.keywords: 44e46590-c7af-e371-28b4-890028cf955b, DXGI_ADAPTER_DESC1, DXGI_ADAPTER_DESC1 structure [DXGI], direct3ddxgi.dxgi_adapter_desc1, dxgi/DXGI_ADAPTER_DESC1
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
req.typenames: DXGI_ADAPTER_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_ADAPTER_DESC1
 - dxgi/DXGI_ADAPTER_DESC1
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
 - DXGI_ADAPTER_DESC1
---

# DXGI_ADAPTER_DESC1 structure


## -description

Describes an adapter (or video card) using DXGI 1.1.

## -struct-fields

### -field Description

Type: <b>WCHAR[128]</b>

A string that contains the adapter description. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a> returns “Software Adapter” for the description string.

### -field VendorId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID or ACPI ID of the adapter's hardware vendor. If this value is less than or equal to 0xFFFF, it is a PCI ID; otherwise, it is an ACPI ID. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a> returns zero for this value.

### -field DeviceId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID or ACPI ID of the adapter's hardware device. If <b>VendorId</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a> returns zero for this value.

### -field SubSysId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID or ACPI ID of the adapter's hardware subsystem. If <b>VendorId</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a> returns zero for this value.

### -field Revision

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The adapter's PCI or ACPI revision number. If <b>VendorId</b> is a PCI ID, it is a PCI device revision number; otherwise, it is an ACPI device revision number. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a> returns zero for this value.

### -field DedicatedVideoMemory

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of dedicated video memory that are not shared with the CPU.

### -field DedicatedSystemMemory

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.

### -field SharedSystemMemory

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.

### -field AdapterLuid

Type: <b><a href="/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a></b>

A unique value that identifies the adapter. See <a href="/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value of the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag">DXGI_ADAPTER_FLAG</a> enumerated type that describes the adapter type.  The <b>DXGI_ADAPTER_FLAG_REMOTE</b> flag is reserved.

## -remarks

The <b>DXGI_ADAPTER_DESC1</b> structure provides a DXGI 1.1 description of an adapter.  This structure is initialized by using the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">IDXGIAdapter1::GetDesc1</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">IDXGIAdapter1::GetDesc1</a>