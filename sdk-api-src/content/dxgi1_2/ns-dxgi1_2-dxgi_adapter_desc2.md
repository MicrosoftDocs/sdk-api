---
UID: NS:dxgi1_2.DXGI_ADAPTER_DESC2
title: DXGI_ADAPTER_DESC2
author: windows-sdk-content
description: Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.2.
old-location: direct3ddxgi\dxgi_adapter_desc2.htm
tech.root: direct3ddxgi
ms.assetid: AE34913A-84D8-49DB-A736-15AECA9989F9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DXGI_ADAPTER_DESC2, DXGI_ADAPTER_DESC2 structure [DXGI], direct3ddxgi.dxgi_adapter_desc2, dxgi1_2/DXGI_ADAPTER_DESC2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_ADAPTER_DESC2
product: Windows
targetos: Windows
req.typenames: DXGI_ADAPTER_DESC2
req.redist: 
---

# DXGI_ADAPTER_DESC2 structure


## -description


Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.2.


## -struct-fields




### -field Description

A string that contains the adapter description.


### -field VendorId

The PCI ID of the hardware vendor.


### -field DeviceId

The PCI ID of the hardware device.


### -field SubSysId

The PCI ID of the sub system.


### -field Revision

The PCI ID of the revision number of the adapter.


### -field DedicatedVideoMemory

The number of bytes of dedicated video memory that are not shared with the CPU.


### -field DedicatedSystemMemory

The number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.


### -field SharedSystemMemory

The number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.


### -field AdapterLuid

A unique value that identifies the adapter. See <a href="https://msdn.microsoft.com/564bcc9a-943b-4ad9-aeaa-0af4c3d3da0c">LUID</a> for a definition of the structure. <b>LUID</b> is defined in dxgi.h.


### -field Flags

A value of the <a href="https://msdn.microsoft.com/9c3c78cd-4f4e-4753-969a-54ea63583be1">DXGI_ADAPTER_FLAG</a> enumerated type that describes the adapter type.  The <b>DXGI_ADAPTER_FLAG_REMOTE</b> flag is reserved.


### -field GraphicsPreemptionGranularity

A value of the <a href="https://msdn.microsoft.com/B1372869-EFDE-49DD-BCF8-D4F59AFE8E7E">DXGI_GRAPHICS_PREEMPTION_GRANULARITY</a> enumerated type that describes the granularity level at which the GPU can be preempted from performing its current graphics rendering task.


### -field ComputePreemptionGranularity

A value of the <a href="https://msdn.microsoft.com/DEE6E26D-B4BB-4832-9CFC-4167F399BC65">DXGI_COMPUTE_PREEMPTION_GRANULARITY</a> enumerated type that describes the granularity level at which the GPU can be preempted from performing its current compute task.


## -remarks



The <b>DXGI_ADAPTER_DESC2</b> structure provides a DXGI 1.2 description of an adapter.  This structure is initialized by using the <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">IDXGIAdapter2::GetDesc2</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">IDXGIAdapter2::GetDesc2</a>
 

 

