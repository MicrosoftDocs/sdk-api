---
UID: NS:dxgi.DXGI_ADAPTER_DESC
title: DXGI_ADAPTER_DESC
author: windows-sdk-content
description: Describes an adapter (or video card) by using DXGI 1.0.
old-location: direct3ddxgi\dxgi_adapter_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_adapter_desc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXGI_ADAPTER_DESC, DXGI_ADAPTER_DESC structure [DXGI], aa379230-8fa1-e846-2745-b4f13f26ee19, direct3ddxgi.dxgi_adapter_desc, dxgi/DXGI_ADAPTER_DESC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: DXGI_ADAPTER_DESC
req.redist: 
---

# DXGI_ADAPTER_DESC structure


## -description


Describes an adapter (or video card) by using DXGI 1.0.


## -struct-fields




### -field Description

Type: <b>WCHAR[128]</b>

A string that contains the adapter description. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a> returns “Software Adapter” for the description string.


### -field VendorId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the hardware vendor. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a> returns zeros for the PCI ID of the hardware vendor.


### -field DeviceId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the hardware device. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a> returns zeros for the PCI ID of the hardware device.


### -field SubSysId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the sub system. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a> returns zeros for the PCI ID of the sub system.


### -field Revision

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the revision number of the adapter. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a> returns zeros for the PCI ID of the revision number of the adapter.


### -field DedicatedVideoMemory

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The number of bytes of dedicated video memory that are not shared with the CPU.


### -field DedicatedSystemMemory

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.


### -field SharedSystemMemory

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.


### -field AdapterLuid

Type: <b><a href="https://msdn.microsoft.com/564bcc9a-943b-4ad9-aeaa-0af4c3d3da0c">LUID</a></b>

A unique value that identifies the adapter. See <a href="https://msdn.microsoft.com/564bcc9a-943b-4ad9-aeaa-0af4c3d3da0c">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.


## -remarks



The <b>DXGI_ADAPTER_DESC</b> structure provides a description of an adapter.  This structure is initialized by using the <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">IDXGIAdapter::GetDesc</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

