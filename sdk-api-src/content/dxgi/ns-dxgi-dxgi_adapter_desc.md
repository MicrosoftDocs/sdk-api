---
UID: NS:dxgi.DXGI_ADAPTER_DESC
title: DXGI_ADAPTER_DESC (dxgi.h)
description: Describes an adapter (or video card) by using DXGI 1.0.helpviewer_keywords: ["DXGI_ADAPTER_DESC","DXGI_ADAPTER_DESC structure [DXGI]","aa379230-8fa1-e846-2745-b4f13f26ee19","direct3ddxgi.dxgi_adapter_desc","dxgi/DXGI_ADAPTER_DESC"]
old-location: direct3ddxgi\dxgi_adapter_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_adapter_desc.htm
ms.date: 12/05/2018
ms.keywords: DXGI_ADAPTER_DESC, DXGI_ADAPTER_DESC structure [DXGI], aa379230-8fa1-e846-2745-b4f13f26ee19, direct3ddxgi.dxgi_adapter_desc, dxgi/DXGI_ADAPTER_DESC
f1_keywords:
- dxgi/DXGI_ADAPTER_DESC
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DXGI.h
api_name:
- DXGI_ADAPTER_DESC
targetos: Windows
req.typenames: DXGI_ADAPTER_DESC
req.redist: 
ms.custom: 19H1
---

# DXGI_ADAPTER_DESC structure


## -description


Describes an adapter (or video card) by using DXGI 1.0.


## -struct-fields




### -field Description

Type: <b>WCHAR[128]</b>

A string that contains the adapter description. On <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a> returns “Software Adapter” for the description string.


### -field VendorId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID of the hardware vendor. On <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a> returns zeros for the PCI ID of the hardware vendor.


### -field DeviceId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID of the hardware device. On <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a> returns zeros for the PCI ID of the hardware device.


### -field SubSysId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID of the sub system. On <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a> returns zeros for the PCI ID of the sub system.


### -field Revision

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The PCI ID of the revision number of the adapter. On <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a> returns zeros for the PCI ID of the revision number of the adapter.


### -field DedicatedVideoMemory

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of dedicated video memory that are not shared with the CPU.


### -field DedicatedSystemMemory

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.


### -field SharedSystemMemory

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.


### -field AdapterLuid

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a></b>

A unique value that identifies the adapter. See <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.


## -remarks



The <b>DXGI_ADAPTER_DESC</b> structure provides a description of an adapter.  This structure is initialized by using the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">IDXGIAdapter::GetDesc</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
 

 

