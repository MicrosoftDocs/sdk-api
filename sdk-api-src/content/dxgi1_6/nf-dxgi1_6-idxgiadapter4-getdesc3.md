---
UID: NF:dxgi1_6.IDXGIAdapter4.GetDesc3
title: IDXGIAdapter4::GetDesc3
author: windows-sdk-content
description: Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 description of an adapter or video card. This description includes information about ACG compatibility.
old-location: direct3ddxgi\idxgiadapter4_getdesc3.htm
old-project: direct3ddxgi
ms.assetid: 2C6C215C-8CD6-4650-A851-B82068E0F252
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetDesc3, GetDesc3 method [DXGI], GetDesc3 method [DXGI],IDXGIAdapter4 interface, IDXGIAdapter4 interface [DXGI],GetDesc3 method, IDXGIAdapter4.GetDesc3, IDXGIAdapter4::GetDesc3, direct3ddxgi.idxgiadapter4_getdesc3, dxgi1_6/IDXGIAdapter4::GetDesc3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter4.GetDesc3
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter4::GetDesc3


## -description


Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 description of an adapter or video card. This description includes information about ACG compatibility.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/A04B37C9-9F83-4812-AAF6-14FA49976051">DXGI_ADAPTER_DESC3</a> structure that describes the adapter.  
	    This parameter must not be <b>NULL</b>. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, early versions of  <b>GetDesc3</b> (<a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a>, and <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a>) return zeros for the PCI ID in the <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of the adapter description structure and “Software Adapter” for the description string in the <b>Description</b> member. <b>GetDesc3</b> and <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">GetDesc2</a> return the actual feature level 9 hardware values in these members.


## -returns



Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.  
          




## -remarks



Use the <b>GetDesc3</b> method to get a DXGI 1.6 description of an adapter.  To get a DXGI 1.2 description, use the <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">IDXGIAdapter2::GetDesc2</a> method. To get a DXGI 1.1 description, use the <a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">IDXGIAdapter1::GetDesc1</a> method. To get a DXGI 1.0 description, use the <a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">IDXGIAdapter::GetDesc</a> method.

The Windows Display Driver Model (WDDM) scheduler can preempt the graphics processing unit (GPU)'s execution of application tasks. The granularity at which the GPU can be preempted from performing its current task in the WDDM 1.1 or earlier driver model is a direct memory access (DMA) buffer for graphics tasks or a compute packet for compute tasks. The GPU can switch between tasks only after it completes the currently executing unit of work, a DMA buffer or a compute packet. 

A DMA buffer is the largest independent unit of graphics work that the WDDM scheduler can submit to the GPU. This buffer contains a set of GPU instructions that the WDDM driver and GPU use. A compute packet is the largest independent unit of compute work that the WDDM scheduler can submit to the GPU. A compute packet contains dispatches (for example, calls to the <a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">ID3D11DeviceContext::Dispatch</a> method), which contain thread groups. The WDDM 1.2 or later driver model allows the GPU to be preempted at finer granularity levels than a DMA buffer or compute packet. You can use the <b>GetDesc3</b> or <a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">GetDesc2</a> methods to retrieve the granularity levels for graphics and compute tasks.




## -see-also




<a href="https://msdn.microsoft.com/176958F9-94C8-4F80-B9A4-96BC9634292E">IDXGIAdapter4</a>
 

 

