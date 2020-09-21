---
UID: NF:d3d11_4.ID3D11Device5.OpenSharedFence
title: ID3D11Device5::OpenSharedFence (d3d11_4.h)
description: Opens a handle for a shared fence by using HANDLE and REFIID.
helpviewer_keywords: ["ID3D11Device5 interface [Direct3D 11]","OpenSharedFence method","ID3D11Device5.OpenSharedFence","ID3D11Device5::OpenSharedFence","OpenSharedFence","OpenSharedFence method [Direct3D 11]","OpenSharedFence method [Direct3D 11]","ID3D11Device5 interface","d3d11_4/ID3D11Device5::OpenSharedFence","direct3d11.id3d11device5_opensharedfence"]
old-location: direct3d11\id3d11device5_opensharedfence.htm
tech.root: direct3d11
ms.assetid: 3EB1BA51-61CB-4389-84A9-77DAC9815AC7
ms.date: 12/05/2018
ms.keywords: ID3D11Device5 interface [Direct3D 11],OpenSharedFence method, ID3D11Device5.OpenSharedFence, ID3D11Device5::OpenSharedFence, OpenSharedFence, OpenSharedFence method [Direct3D 11], OpenSharedFence method [Direct3D 11],ID3D11Device5 interface, d3d11_4/ID3D11Device5::OpenSharedFence, direct3d11.id3d11device5_opensharedfence
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device5::OpenSharedFence
 - d3d11_4/ID3D11Device5::OpenSharedFence
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device5.OpenSharedFence
---

# ID3D11Device5::OpenSharedFence


## -description

Opens a handle for a shared fence by using HANDLE and REFIID.

This member function is a limited version of the Direct3D 12 <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle">ID3D12Device::OpenSharedHandle</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios. Unlike <b>ID3D12Device::OpenSharedHandle</b> which operates on resources, heaps, and fences, the <b>ID3D11Device5::OpenSharedFence</b> function only operates on fences; in Direct3D 11, shared resources are opened with the [ID3D11Device::OpenSharedResource1](../d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1.md) member function.

## -parameters

### -param hFence [in]

Type: <b>HANDLE</b>

The handle that was returned by a call to <a href="/windows/win32/api/d3d11_3/nf-d3d11_3-id3d11fence-createsharedhandle">ID3D11Fence::CreateSharedHandle</a> or <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle">ID3D12Device::CreateSharedHandle</a>.

### -param ReturnedInterface

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the <a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a> interface. The <b>REFIID</b>, or <b>GUID</b>, of the interface can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D11Fence) will get the <b>GUID</b> of the interface to the fence.

### -param ppFence [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11fence">ID3D11Fence</a> interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

[ID3D11Device5](./nn-d3d11_4-id3d11device5.md), [Multi-adapter systems](/windows/win32/direct3d12/multi-engine)