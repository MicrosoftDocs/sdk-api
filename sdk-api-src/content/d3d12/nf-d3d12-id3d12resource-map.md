---
UID: NF:d3d12.ID3D12Resource.Map
title: ID3D12Resource::Map (d3d12.h)
description: Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. Map also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU.
helpviewer_keywords: ["ID3D12Resource interface","Map method","ID3D12Resource.Map","ID3D12Resource::Map","Map","Map method","Map method","ID3D12Resource interface","d3d12/ID3D12Resource::Map","direct3d12.id3d12resource_map"]
old-location: direct3d12\id3d12resource_map.htm
tech.root: direct3d12
ms.assetid: 71E43B63-9C84-4E4B-A43D-92B958C8AAF5
ms.date: 08/10/2022
ms.keywords: ID3D12Resource interface,Map method, ID3D12Resource.Map, ID3D12Resource::Map, Map, Map method, Map method,ID3D12Resource interface, d3d12/ID3D12Resource::Map, direct3d12.id3d12resource_map
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
 - ID3D12Resource::Map
 - d3d12/ID3D12Resource::Map
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
 - ID3D12Resource.Map
---

# ID3D12Resource::Map


## -description

Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. <b>Map</b> also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU.

## -parameters

### -param Subresource

Type: <b>UINT</b>

Specifies the index number of the subresource.

### -param pReadRange [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_range">D3D12_RANGE</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_range">D3D12_RANGE</a> structure that describes the range of memory to access.

This indicates the region the CPU might read, and the coordinates are subresource-relative. A null pointer indicates the entire subresource might be read by the CPU. It is valid to specify the CPU won't read any data by passing a range where <b>End</b> is less than or equal to <b>Begin</b>.

### -param ppData [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the resource data.

A null pointer is valid and is useful to cache a CPU virtual address range for methods like <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a>. When <i>ppData</i> is not NULL, the pointer returned is never offset by any values in <i>pReadRange</i>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

<b>Map</b> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap">Unmap</a> can be called by multiple threads safely. Nested <b>Map</b> calls are supported and are ref-counted. The first call to <b>Map</b> allocates a CPU virtual address range for the resource. The last call to <b>Unmap</b> deallocates the CPU virtual address range. The CPU virtual address is commonly returned to the application; but manipulating the contents of textures with unknown layouts precludes disclosing the CPU virtual address. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a> for more details. Applications cannot rely on the address being consistent, unless <b>Map</b> is persistently nested.


Pointers returned by <b>Map</b> are not guaranteed to have all the capabilities of normal pointers, but most applications won't notice a difference in normal usage. For example, pointers with WRITE_COMBINE behavior have weaker CPU memory ordering guarantees than WRITE_BACK behavior. Memory accessible by both CPU and GPU are not guaranteed to share the same atomic memory guarantees that the CPU has, due to PCIe limitations. Use fences for synchronization.


There are two usage model categories for <b>Map</b>, simple and advanced. The simple usage models maximize tool performance, so applications are recommended to stick with the simple models until the advanced models are proven to be required by the app.


<h3><a id="Simple_Usage_Models"></a><a id="simple_usage_models"></a><a id="SIMPLE_USAGE_MODELS"></a>Simple Usage Models</h3>
Applications should stick to the heap type abstractions of UPLOAD, DEFAULT, and READBACK, in order to support all adapter architectures reasonably well.

Applications should avoid CPU reads from pointers to resources on UPLOAD heaps, even accidently. CPU reads will work, but are prohibitively slow on many common GPU architectures, so consider the following:

<ul>
<li>
Don't make the CPU read from resources associated with heaps that are D3D12_HEAP_TYPE_UPLOAD or have D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE.

</li>
<li>
The memory region to which <b>pData</b> points can be allocated with <a href="/windows/desktop/Memory/memory-protection-constants">PAGE_WRITECOMBINE</a>, and your app must honor all restrictions that are associated with such memory.

</li>
<li>
Even the following C++ code can read from memory and trigger the performance penalty because the code can expand to the following x86 assembly code.
              

C++ code:
              


```
*((int*)MappedResource.pData) = 0;
```


x86 assembly code:
              


```
AND DWORD PTR [EAX],0
```


</li>
<li>
Use the appropriate optimization settings and language constructs to help avoid this performance penalty. For example, you can avoid the xor optimization by using a <b>volatile</b> pointer or by optimizing for code speed instead of code size.

</li>
</ul>
Applications are encouraged to leave resources unmapped while the CPU will not modify them, and use tight, accurate ranges at all times. This enables the fastest modes for tools, like <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics">Graphics Debugging</a> and the debug layer. Such tools need to track all CPU modifications to memory that the GPU could read.


<h3><a id="Advanced_Usage_Models"></a><a id="advanced_usage_models"></a><a id="ADVANCED_USAGE_MODELS"></a>Advanced Usage Models</h3>
Resources on CPU-accessible heaps can be persistently mapped, meaning <b>Map</b> can be called once, immediately after resource creation. <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap">Unmap</a> never needs to be called, but the address returned from <b>Map</b> must no longer be used after the last reference to the resource is released. When using persistent map, the application must ensure the CPU finishes writing data into memory before the GPU executes a command list that reads or writes the memory. In common scenarios, the application merely must write to memory before calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ExecuteCommandLists</a>; but using a fence to delay command list execution works as well.


All CPU-accessible memory types support persistent mapping usage, where the resource is mapped but then never unmapped, provided the application does not access the pointer after the resource has been disposed.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12Resource::Map</b> as follows:
        

Copy triangle data to the vertex buffer.


```cpp
// Copy the triangle data to the vertex buffer.
UINT8* pVertexDataBegin;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
m_vertexBuffer->Unmap(0, nullptr);

```


 Create an upload heap for the constant buffers.


```cpp
// Create an upload heap for the constant buffers.
ThrowIfFailed(pDevice->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(ConstantBuffer) * m_cityRowCount * m_cityColumnCount),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    nullptr,
    IID_PPV_ARGS(&m_cbvUploadHeap)));

// Map the constant buffers. Note that unlike D3D11, the resource 
// does not need to be unmapped for use by the GPU. In this sample, 
// the resource stays 'permanently' mapped to avoid overhead with 
// mapping/unmapping each frame.
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_cbvUploadHeap->Map(0, &readRange, reinterpret_cast<void**>(&m_pConstantBuffers)));

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>



<a href="/windows/desktop/direct3d12/subresources">Subresources</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap">Unmap</a>
