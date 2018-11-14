---
UID: NF:dxgi1_2.IDXGIAdapter2.GetDesc2
title: IDXGIAdapter2::GetDesc2
author: windows-sdk-content
description: Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.2 description of an adapter or video card.
old-location: direct3ddxgi\idxgiadapter2_getdesc2.htm
tech.root: direct3ddxgi
ms.assetid: DC1A054D-4092-4865-A6EF-B936891AA470
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetDesc2, GetDesc2 method [DXGI], GetDesc2 method [DXGI],IDXGIAdapter2 interface, IDXGIAdapter2 interface [DXGI],GetDesc2 method, IDXGIAdapter2.GetDesc2, IDXGIAdapter2::GetDesc2, direct3ddxgi.idxgiadapter2_getdesc2, dxgi1_2/IDXGIAdapter2::GetDesc2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIAdapter2.GetDesc2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_2.h
: 
- IDXGIAdapter2.GetDesc2
: 
---

# IDXGIAdapter2::GetDesc2


## -description


Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.2 description of an adapter or video card. This description includes information about the granularity at which the graphics processing unit (GPU) can be preempted from performing its current task.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a> structure that describes the adapter.  
      This parameter must not be <b>NULL</b>. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, earlier versions of  <b>GetDesc2</b> (<a href="https://msdn.microsoft.com/en-us/library/Bb174526(v=VS.85).aspx">GetDesc</a> and <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a>) return zeros for the PCI ID in the <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of the adapter description structure and “Software Adapter” for the description string in the <b>Description</b> member. <b>GetDesc2</b> returns the actual feature level 9 hardware values in these members.


## -returns



Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.  
        




## -remarks



Use the <b>GetDesc2</b> method to get a DXGI 1.2 description of an adapter.  To get a DXGI 1.1 description, use the <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">IDXGIAdapter1::GetDesc1</a> method. To get a DXGI 1.0 description, use the <a href="https://msdn.microsoft.com/en-us/library/Bb174526(v=VS.85).aspx">IDXGIAdapter::GetDesc</a> method.

The Windows Display Driver Model (WDDM) scheduler can preempt the GPU's execution of application tasks. The granularity at which the GPU can be preempted from performing its current task in the WDDM 1.1 or earlier driver model is a direct memory access (DMA) buffer for graphics tasks or a compute packet for compute tasks. The GPU can switch between tasks only after it completes the currently executing unit of work, a DMA buffer or a compute packet. 

A DMA buffer is the largest independent unit of graphics work that the WDDM scheduler can submit to the GPU. This buffer contains a set of GPU instructions that the WDDM driver and GPU use. A compute packet is the largest independent unit of compute work that the WDDM scheduler can submit to the GPU. A compute packet contains dispatches (for example, calls to the <a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">ID3D11DeviceContext::Dispatch</a> method), which contain thread groups. The WDDM 1.2 or later driver model allows the GPU to be preempted at finer granularity levels than a DMA buffer or compute packet. You can use the <b>GetDesc2</b> method to retrieve the granularity levels for graphics and compute tasks.




## -see-also




<a href="https://msdn.microsoft.com/9AAD133C-CE40-498B-827F-2B35C7C15B8C">IDXGIAdapter2</a>
 

 

