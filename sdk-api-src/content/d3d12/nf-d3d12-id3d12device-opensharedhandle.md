---
UID: NF:d3d12.ID3D12Device.OpenSharedHandle
title: ID3D12Device::OpenSharedHandle (d3d12.h)
description: Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
helpviewer_keywords: ["ID3D12Device interface","OpenSharedHandle method","ID3D12Device.OpenSharedHandle","ID3D12Device::OpenSharedHandle","OpenSharedHandle","OpenSharedHandle method","OpenSharedHandle method","ID3D12Device interface","d3d12/ID3D12Device::OpenSharedHandle","direct3d12.id3d12device_opensharedhandle"]
old-location: direct3d12\id3d12device_opensharedhandle.htm
tech.root: direct3d12
ms.assetid: 4F428B06-2906-4ED6-BB75-5DACF2155FA9
ms.date: 12/05/2018
ms.keywords: ID3D12Device interface,OpenSharedHandle method, ID3D12Device.OpenSharedHandle, ID3D12Device::OpenSharedHandle, OpenSharedHandle, OpenSharedHandle method, OpenSharedHandle method,ID3D12Device interface, d3d12/ID3D12Device::OpenSharedHandle, direct3d12.id3d12device_opensharedhandle
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::OpenSharedHandle
 - d3d12/ID3D12Device::OpenSharedHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.OpenSharedHandle
---

# ID3D12Device::OpenSharedHandle


## -description

Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.

## -parameters

### -param NTHandle [in]

Type: <b>HANDLE</b>

The handle that was output by the call to 
            <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle">ID3D12Device::CreateSharedHandle</a>.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for one of the following interfaces:
            

<ul>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>
</li>
</ul>
The <b>REFIID</b>, or <b>GUID</b>, of the interface can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12Heap) will get the <b>GUID</b> of the interface to a resource.

### -param ppvObj [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to one of the following interfaces:
            

<ul>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>
</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>

