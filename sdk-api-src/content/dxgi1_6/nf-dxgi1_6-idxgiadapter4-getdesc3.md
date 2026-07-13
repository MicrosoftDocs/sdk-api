---
UID: NF:dxgi1_6.IDXGIAdapter4.GetDesc3
title: IDXGIAdapter4::GetDesc3 (dxgi1_6.h)
description: Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 description of an adapter or video card. This description includes information about ACG compatibility.
helpviewer_keywords: ["GetDesc3","GetDesc3 method [DXGI]","GetDesc3 method [DXGI]","IDXGIAdapter4 interface","IDXGIAdapter4 interface [DXGI]","GetDesc3 method","IDXGIAdapter4.GetDesc3","IDXGIAdapter4::GetDesc3","direct3ddxgi.idxgiadapter4_getdesc3","dxgi1_6/IDXGIAdapter4::GetDesc3"]
old-location: direct3ddxgi\idxgiadapter4_getdesc3.htm
tech.root: direct3ddxgi
ms.assetid: 2C6C215C-8CD6-4650-A851-B82068E0F252
ms.date: 12/05/2018
ms.keywords: GetDesc3, GetDesc3 method [DXGI], GetDesc3 method [DXGI],IDXGIAdapter4 interface, IDXGIAdapter4 interface [DXGI],GetDesc3 method, IDXGIAdapter4.GetDesc3, IDXGIAdapter4::GetDesc3, direct3ddxgi.idxgiadapter4_getdesc3, dxgi1_6/IDXGIAdapter4::GetDesc3
req.header: dxgi1_6.h
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
req.lib: DXGI.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter4::GetDesc3
 - dxgi1_6/IDXGIAdapter4::GetDesc3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter4.GetDesc3
---

# IDXGIAdapter4::GetDesc3


## -description

Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 description of an adapter or video card. This description includes information about ACG compatibility.

## -parameters

### -param pDesc [out]

A pointer to a <a href="/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3">DXGI_ADAPTER_DESC3</a> structure that describes the adapter.  
	    This parameter must not be <b>NULL</b>. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, early versions of  <b>GetDesc3</b> (<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">GetDesc1</a>, and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a>) return zeros for <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of the adapter description structure and “Software Adapter” for the description string in the <b>Description</b> member. <b>GetDesc3</b> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">GetDesc2</a> return the actual feature level 9 hardware values in these members.

## -returns

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.

## -remarks

Use the <b>GetDesc3</b> method to get a DXGI 1.6 description of an adapter.  To get a DXGI 1.2 description, use the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">IDXGIAdapter2::GetDesc2</a> method. To get a DXGI 1.1 description, use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter1-getdesc1">IDXGIAdapter1::GetDesc1</a> method. To get a DXGI 1.0 description, use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">IDXGIAdapter::GetDesc</a> method.

The Windows Display Driver Model (WDDM) scheduler can preempt the graphics processing unit (GPU)'s execution of application tasks. The granularity at which the GPU can be preempted from performing its current task in the WDDM 1.1 or earlier driver model is a direct memory access (DMA) buffer for graphics tasks or a compute packet for compute tasks. The GPU can switch between tasks only after it completes the currently executing unit of work, a DMA buffer or a compute packet. 

A DMA buffer is the largest independent unit of graphics work that the WDDM scheduler can submit to the GPU. This buffer contains a set of GPU instructions that the WDDM driver and GPU use. A compute packet is the largest independent unit of compute work that the WDDM scheduler can submit to the GPU. A compute packet contains dispatches (for example, calls to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">ID3D11DeviceContext::Dispatch</a> method), which contain thread groups. The WDDM 1.2 or later driver model allows the GPU to be preempted at finer granularity levels than a DMA buffer or compute packet. You can use the <b>GetDesc3</b> or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">GetDesc2</a> methods to retrieve the granularity levels for graphics and compute tasks.

## -see-also

<a href="/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4">IDXGIAdapter4</a>