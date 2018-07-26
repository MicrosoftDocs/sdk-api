---
UID: NF:d3d12.ID3D12Resource.Map
title: ID3D12Resource::Map
author: windows-sdk-content
description: Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. Map also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU.
old-location: direct3d12\id3d12resource_map.htm
old-project: direct3d12
ms.assetid: 71E43B63-9C84-4E4B-A43D-92B958C8AAF5
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12Resource interface,Map method, ID3D12Resource.Map, ID3D12Resource::Map, Map, Map method, Map method,ID3D12Resource interface, d3d12/ID3D12Resource::Map, direct3d12.id3d12resource_map
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Resource.Map
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Resource::Map


## -description


Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. <b>Map</b> also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU.



## -parameters




### -param Subresource

Type: <b>UINT</b>

Specifies the index number of the subresource.


### -param pReadRange [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/E8A66EC7-DB20-475D-BCD1-6C164FF39D24">D3D12_RANGE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/E8A66EC7-DB20-475D-BCD1-6C164FF39D24">D3D12_RANGE</a> structure that describes the range of memory to access.

This indicates the region the CPU might read, and the coordinates are subresource-relative. A null pointer indicates the entire subresource might be read by the CPU. It is valid to specify the CPU won't read any data by passing a range where <b>End</b> is less than or equal to <b>Begin</b>.



### -param ppData [out, optional]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the resource data.

A null pointer is valid and is useful to cache a CPU virtual address range for methods like <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a>. When <i>ppData</i> is not NULL, the pointer returned is never offset by any values in <i>pReadRange</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



<b>Map</b> and <a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a> can be called by multiple threads safely. Nested <b>Map</b> calls are supported and are ref-counted. The first call to <b>Map</b> allocates a CPU virtual address range for the resource. The last call to <b>Unmap</b> deallocates the CPU virtual address range. The CPU virtual address is commonly returned to the application; but manipulating the contents of textures with unknown layouts precludes disclosing the CPU virtual address. See <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a> for more details. Applications cannot rely on the address being consistent, unless <b>Map</b> is persistently nested.


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
The memory region to which <b>pData</b> points can be allocated with <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">PAGE_WRITECOMBINE</a>, and your app must honor all restrictions that are associated with such memory.

</li>
<li>
Even the following C++ code can read from memory and trigger the performance penalty because the code can expand to the following x86 assembly code.
              

C++ code:
              

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>*((int*)MappedResource.pData) = 0;</pre>
</td>
</tr>
</table></span></div>
x86 assembly code:
              

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>AND DWORD PTR [EAX],0</pre>
</td>
</tr>
</table></span></div>
</li>
<li>
Use the appropriate optimization settings and language constructs to help avoid this performance penalty. For example, you can avoid the xor optimization by using a <b>volatile</b> pointer or by optimizing for code speed instead of code size.

</li>
</ul>
Applications are encouraged to leave resources unmapped while the CPU will not modify them, and use tight, accurate ranges at all times. This enables the fastest modes for tools, like <a href="https://msdn.microsoft.com/en-us/library/hh315751.aspx">Graphics Debugging</a> and the debug layer. Such tools need to track all CPU modifications to memory that the GPU could read.

Resources on D3D12_HEAP_TYPE_READBACK heaps do not support persistent map. <b>Map</b> and <a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a> must be called between CPU and GPU accesses to the same memory address on some system architectures, when the page caching behavior is write-back. <b>Map</b> and <b>Unmap</b> invalidate and flush the last level CPU cache on some ARM systems, to marshal data between the CPU and GPU through memory addresses with write-back behavior.


<h3><a id="Advanced_Usage_Models"></a><a id="advanced_usage_models"></a><a id="ADVANCED_USAGE_MODELS"></a>Advanced Usage Models</h3>
Resources on D3D12_HEAP_TYPE_UPLOAD heaps can be persistently mapped, meaning <b>Map</b> can be called once, immediately after resource creation. <a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a> never needs to be called, but the address returned from <b>Map</b> must no longer be used after the last reference to the resource is released. When using persistent map, the application must ensure the CPU finishes writing data into memory before the GPU executes a command list that reads the memory. In common scenarios, the application merely must write to memory before calling <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandLists</a>; but using a fence to delay command list execution works as well.


Applications may understand the adapter architectural details and use custom heaps to write optimizations for UMA architectures, multi-engine applications, multi-adapter applications, and other less common scenarios. Persistent map can be used on the custom heap types when the adapter architectures supports it. Heaps with write-combine properties always support persistent map, and heaps with write-back properties support persistent map on non-ARM systems.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12Resource::Map</b> as follows:
        

Copy triangle data to the vertex buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Copy the triangle data to the vertex buffer.
UINT8* pVertexDataBegin;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_vertexBuffer-&gt;Map(0, &amp;readRange, reinterpret_cast&lt;void**&gt;(&amp;pVertexDataBegin)));
memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
m_vertexBuffer-&gt;Unmap(0, nullptr);
</pre>
</td>
</tr>
</table></span></div>
 Create an upload heap for the constant buffers.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create an upload heap for the constant buffers.
ThrowIfFailed(pDevice-&gt;CreateCommittedResource(
    &amp;CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &amp;CD3DX12_RESOURCE_DESC::Buffer(sizeof(ConstantBuffer) * m_cityRowCount * m_cityColumnCount),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    nullptr,
    IID_PPV_ARGS(&amp;m_cbvUploadHeap)));

// Map the constant buffers. Note that unlike D3D11, the resource 
// does not need to be unmapped for use by the GPU. In this sample, 
// the resource stays 'permenantly' mapped to avoid overhead with 
// mapping/unmapping each frame.
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_cbvUploadHeap-&gt;Map(0, &amp;readRange, reinterpret_cast&lt;void**&gt;(&amp;m_pConstantBuffers)));
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>



<a href="https://msdn.microsoft.com/C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F">Subresources</a>



<a href="https://msdn.microsoft.com/EB0E3936-47CC-4FDC-BF17-A506AC8E4C15">Unmap</a>
 

 

