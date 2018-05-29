---
UID: NS:dxgi.DXGI_ADAPTER_DESC1
title: DXGI_ADAPTER_DESC1
author: windows-sdk-content
description: Describes an adapter (or video card) using DXGI 1.1.
old-location: direct3ddxgi\dxgi_adapter_desc1.htm
old-project: direct3ddxgi
ms.assetid: 0ae3bdb1-b122-439a-8f62-c831a9dd87e2
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: 44e46590-c7af-e371-28b4-890028cf955b, DXGI_ADAPTER_DESC1, DXGI_ADAPTER_DESC1 structure [DXGI], direct3ddxgi.dxgi_adapter_desc1, dxgi/DXGI_ADAPTER_DESC1
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DXGI_ADAPTER_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DXGI.h
api_name:
-	DXGI_ADAPTER_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_ADAPTER_DESC1 structure


## -description


Describes an adapter (or video card) using DXGI 1.1.


## -struct-fields




### -field Description

Type: <b>WCHAR[128]</b>

A string that contains the adapter description. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a> returns “Software Adapter” for the description string.


### -field VendorId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the hardware vendor. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a> returns zeros for the PCI ID of the hardware vendor.


### -field DeviceId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the hardware device. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a> returns zeros for the PCI ID of the hardware device.


### -field SubSysId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the sub system. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a> returns zeros for the PCI ID of the sub system.


### -field Revision

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The PCI ID of the revision number of the adapter. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a> returns zeros for the PCI ID of the revision number of the adapter.


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

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a></b>

A unique value that identifies the adapter. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value of the <a href="https://msdn.microsoft.com/9c3c78cd-4f4e-4753-969a-54ea63583be1">DXGI_ADAPTER_FLAG</a> enumerated type that describes the adapter type.  The <b>DXGI_ADAPTER_FLAG_REMOTE</b> flag is reserved.


## -remarks



The <b>DXGI_ADAPTER_DESC1</b> structure provides a DXGI 1.1 description of an adapter.  This structure is initialized by using the <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">IDXGIAdapter1::GetDesc1</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">IDXGIAdapter1::GetDesc1</a>
 

 

