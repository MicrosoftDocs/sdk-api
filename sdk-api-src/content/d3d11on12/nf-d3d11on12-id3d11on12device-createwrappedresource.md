---
UID: NF:d3d11on12.ID3D11On12Device.CreateWrappedResource
title: ID3D11On12Device::CreateWrappedResource (d3d11on12.h)
description: This method creates D3D11 resources for use with D3D 11on12.
helpviewer_keywords: ["CreateWrappedResource","CreateWrappedResource method","CreateWrappedResource method","ID3D11On12Device interface","ID3D11On12Device interface","CreateWrappedResource method","ID3D11On12Device.CreateWrappedResource","ID3D11On12Device::CreateWrappedResource","d3d11on12/ID3D11On12Device::CreateWrappedResource","direct3d12.id3d11on12device_createwrappedresource"]
old-location: direct3d12\id3d11on12device_createwrappedresource.htm
tech.root: direct3d12
ms.assetid: 83B37B0A-9965-40F6-A5B1-8B4DC21BC455
ms.date: 12/05/2018
ms.keywords: CreateWrappedResource, CreateWrappedResource method, CreateWrappedResource method,ID3D11On12Device interface, ID3D11On12Device interface,CreateWrappedResource method, ID3D11On12Device.CreateWrappedResource, ID3D11On12Device::CreateWrappedResource, d3d11on12/ID3D11On12Device::CreateWrappedResource, direct3d12.id3d11on12device_createwrappedresource
req.header: d3d11on12.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11On12Device::CreateWrappedResource
 - d3d11on12/ID3D11On12Device::CreateWrappedResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11On12Device.CreateWrappedResource
---

# ID3D11On12Device::CreateWrappedResource


## -description

This method creates D3D11 resources for use with D3D 11on12.

## -parameters

### -param pResource12 [in]

Type: <b>IUnknown*</b>

A pointer to an already-created D3D12 resource or heap.

### -param pFlags11 [in]

Type: <b>const <a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags">D3D11_RESOURCE_FLAGS</a>*</b>

A <a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags">D3D11_RESOURCE_FLAGS</a> structure that enables an application to override flags that would be inferred by the resource/heap properties.
              The D3D11_RESOURCE_FLAGS structure contains bind flags, misc flags, and CPU access flags.

### -param InState

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a></b>

The use of the resource on input, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> enumeration constants.

### -param OutState

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a></b>

The use of the resource on output, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> enumeration constants.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the wrapped resource interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the wrapped resource can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>) will get the <b>GUID</b> of the interface to a wrapped resource.

### -param ppResource11 [out, optional]

Type: <b>void**</b>

After the method returns, points to the newly created wrapped D3D11 resource or heap.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device">ID3D11On12Device</a>