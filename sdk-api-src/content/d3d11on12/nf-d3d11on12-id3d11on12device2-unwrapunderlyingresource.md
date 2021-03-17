---
UID: NF:d3d11on12.ID3D11On12Device2.UnwrapUnderlyingResource
title: ID3D11On12Device2::UnwrapUnderlyingResource
description: Unwraps a Direct3D 11 resource object, and retrieves it as a Direct3D 12 resource object.
tech.root: direct3d12
ms.date: 01/22/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: D3D11.dll
req.header: d3d11on12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: D3D11.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d11on12.h
api_name:
 - ID3D11On12Device2::UnwrapUnderlyingResource
f1_keywords:
 - ID3D11On12Device2::UnwrapUnderlyingResource
 - d3d11on12/ID3D11On12Device2::UnwrapUnderlyingResource
dev_langs:
 - c++
---

## -description

Unwraps a Direct3D 11 resource object, and retrieves it as a Direct3D 12 resource object.

## -parameters

### -param pResource11 [in]

Type: **[ID3D11Resource](../d3d11/nn-d3d11-id3d11resource.md)\***

The Direct3D 11 resource object to unwrap.

### -param pCommandQueue [in]

Type: **[ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md)\***

The command queue on which your application plans to use the resource. Any pending work accessing the resource causes fence waits to be scheduled on this queue. You can then queue further work on this queue, including a signal on a caller-owned fence.

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in `ppvResource12`.

### -param ppvResource12 [out]

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

A pointer to a memory block that receives a pointer to the Direct3D 12 resource.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

The resource is transitioned to **D3D12_RESOURCE_STATE_COMMON** (if it wasn't already in that state), and appropriate waits are inserted into the command queue (*pCommandQueue*).

There are some restrictions on what can be unwrapped: no keyed mutex resources, no GDI-compatible resources, and no buffers. However, you can use **UnwrapUnderlyingResource** to unwrap resources created through the **[ID3D11On12Device::CreateWrappedResource](./nf-d3d11on12-id3d11on12device-createwrappedresource.md)** method, as well as resources created through [ID3D11Device::CreateTexture2D](../d3d11/nf-d3d11-id3d11device-createtexture2d.md).

In general, you must return the object to Direct3D11on12 before using it again in Direct3D 11 (see [ID3D11On12Device2::ReturnUnderlyingResource](nf-d3d11on12-id3d11on12device2-returnunderlyingresource.md)).

You can also use **UnwrapUnderlyingResource** to unwrap a swapchain buffer. You must also return the resource to Direct3D11on12 before calling **Present** (or otherwise using the resource).

Unwrapping a resource checks out the resource from the Direct3D11On12 translation layer. You may not schedule any translation layer usage (through either version of the API) while the resource is checked out. Check the resource back in (also known as *returning* the resource) with [ID3D11On12Device2::ReturnUnderlyingResource](nf-d3d11on12-id3d11on12device2-returnunderlyingresource.md).

**UnwrapUnderlyingResource** doesn't flush, and it may schedule GPU work. You should flush after calling **UnwrapUnderlyingResource** if you externally wait for completion.

## -see-also

* [ID3D12Device interface](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)
* [ID3D11On12Device2::ReturnUnderlyingResource](nf-d3d11on12-id3d11on12device2-returnunderlyingresource.md)