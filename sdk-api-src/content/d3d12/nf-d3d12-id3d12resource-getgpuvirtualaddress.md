---
UID: NF:d3d12.ID3D12Resource.GetGPUVirtualAddress
title: ID3D12Resource::GetGPUVirtualAddress (d3d12.h)
description: This method returns the GPU virtual address of a buffer resource.
helpviewer_keywords: ["GetGPUVirtualAddress","GetGPUVirtualAddress method","GetGPUVirtualAddress method","ID3D12Resource interface","ID3D12Resource interface","GetGPUVirtualAddress method","ID3D12Resource.GetGPUVirtualAddress","ID3D12Resource::GetGPUVirtualAddress","d3d12/ID3D12Resource::GetGPUVirtualAddress","direct3d12.id3d12resource_getgpuvirtualaddress"]
old-location: direct3d12\id3d12resource_getgpuvirtualaddress.htm
tech.root: direct3d12
ms.assetid: 1B1A345D-D6BD-4DF1-8F10-A209135283AD
ms.date: 12/05/2018
ms.keywords: GetGPUVirtualAddress, GetGPUVirtualAddress method, GetGPUVirtualAddress method,ID3D12Resource interface, ID3D12Resource interface,GetGPUVirtualAddress method, ID3D12Resource.GetGPUVirtualAddress, ID3D12Resource::GetGPUVirtualAddress, d3d12/ID3D12Resource::GetGPUVirtualAddress, direct3d12.id3d12resource_getgpuvirtualaddress
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Resource::GetGPUVirtualAddress
 - d3d12/ID3D12Resource::GetGPUVirtualAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Resource.GetGPUVirtualAddress
---

# ID3D12Resource::GetGPUVirtualAddress


## -description

This method returns the GPU virtual address of a buffer resource.



## -returns

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

This method returns the GPU virtual address.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd synonym of UINT64.

## -remarks

This method is only useful for buffer resources, it will return zero for all texture resources.

For more information on the use of GPU virtual addresses, refer to <a href="/windows/desktop/direct3d12/indirect-drawing">Indirect Drawing</a>. 
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D1211on12</a> sample uses <b>ID3D12Resource::GetGPUVirtualAddress</b> as follows:
        


```cpp
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.StrideInBytes = sizeof(Vertex);
m_vertexBufferView.SizeInBytes = vertexBufferSize;

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>
