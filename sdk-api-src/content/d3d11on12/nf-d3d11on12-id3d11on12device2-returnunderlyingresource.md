---
UID: NF:d3d11on12.ID3D11On12Device2.ReturnUnderlyingResource
title: ID3D11On12Device2::ReturnUnderlyingResource
description: With this method, you can return a Direct3D 11 resource object to Direct3D11On12, and indicate when the resource will be ready to consume.
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
 - ID3D11On12Device2::ReturnUnderlyingResource
f1_keywords:
 - ID3D11On12Device2::ReturnUnderlyingResource
 - d3d11on12/ID3D11On12Device2::ReturnUnderlyingResource
dev_langs:
 - c++
---

## -description

With this method, you can return a Direct3D 11 resource object to Direct3D11On12, and indicate (by way of fences and fence signal values) when the resource will be ready for Direct3D11On12 to consume. You should call **ReturnUnderlyingResource** once Direct3D 12 work has been scheduled.

## -parameters

### -param pResource11 [in]

Type: **[ID3D11Resource](../d3d11/nn-d3d11-id3d11resource.md)\***

The Direct3D 11 resource object that you wish to return.

### -param NumSync [in]

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The number of elements in the arrays pointed to by *pSignalValues* and *ppFences*.

### -param pSignalValues [in]

Type: **[UINT64](/windows/win32/winprog/windows-data-types)\***

A pointer to an array of fence signal values.

### -param ppFences [in]

Type: **[ID3D12Fence](../d3d12/nn-d3d12-id3d12fence.md)\*\***

A pointer to an array of fence objects.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

When you return a resource, you provide a set of fences and fence signal values whose completion indicates that the resource is back in the **D3D12_RESOURCE_STATE_COMMON** state, and ready for Direct3D11On12 to consume it.

In the parallel arrays *pSignalValues* and *ppFences*, include any pending work against the resource. The Direct3D11On12 translation layer defers the waits for these arguments until work is scheduled against the resource.

## -see-also

* [ID3D11On12Device2::UnwrapUnderlyingResource](nf-d3d11on12-id3d11on12device2-unwrapunderlyingresource.md)