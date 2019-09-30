---
UID: NF:d3d12.ID3D12Device.CreateCommittedResource
title: ID3D12Device::CreateCommittedResource (d3d12.h)
author: windows-sdk-content
description: Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
old-location: direct3d12\id3d12device_createcommittedresource.htm
tech.root: direct3d12
ms.assetid: FF9E8F11-F2C5-4A96-8E25-140870D15DA9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateCommittedResource, CreateCommittedResource method, CreateCommittedResource method,ID3D12Device interface, ID3D12Device interface,CreateCommittedResource method, ID3D12Device.CreateCommittedResource, ID3D12Device::CreateCommittedResource, d3d12/ID3D12Device::CreateCommittedResource, direct3d12.id3d12device_createcommittedresource
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12Device.CreateCommittedResource"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateCommittedResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device::CreateCommittedResource


## -description


Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
        


## -parameters




### -param pHeapProperties [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure that provides properties for the resource's heap.
          


### -param HeapFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a></b>

Heap options, as a bitwise-OR'd combination of <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a> enumeration constants.
          


### -param pDesc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure that describes the resource.
          


### -param InitialResourceState

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a></b>

The initial state of the resource, as a bitwise-OR'd combination of <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> enumeration constants.
            

When a resource is created together with a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a>_UPLOAD heap, <i>InitialResourceState</i> must be <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE</a>_GENERIC_READ.
              When a resource is created together with a D3D12_HEAP_TYPE_READBACK heap, <i>InitialResourceState</i> must be D3D12_RESOURCE_STATE_COPY_DEST.
            


### -param pOptimizedClearValue [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value">D3D12_CLEAR_VALUE</a>*</b>

Specifies a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value">D3D12_CLEAR_VALUE</a> that describes the default value for a clear color.
            

<i>pOptimizedClearValue</i> specifies a value for which clear operations are most optimal. When the created resource is a texture with either the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG</a>_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL flags, applications should choose the value that the clear operation will most commonly be called with. Clear operations can be called with other values, but those operations will not be as efficient as when the value matches the one passed into resource creation.
              <i>pOptimizedClearValue</i> must be NULL when used with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>_BUFFER.
            


### -param riidResource

Type: <b><b>REFIID</b></b>

The globally unique identifier (<b>GUID</b>) for the resource interface.
              This is an input parameter.
              The <b>REFIID</b>, or <b>GUID</b>, of the interface to the resource can be obtained by using the __uuidof() macro.
              For example, __uuidof(<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a resource.
            

While riidResource is, most commonly, the GUID for <b>ID3D12Resource</b>, it may be any GUID for any interface.
              If the resource object doesn't support the interface for this GUID, creation will fail with E_NOINTERFACE.
            


### -param ppvResource [out, optional]

Type: <b><b>void</b>**</b>

A pointer to memory that receives the requested interface pointer to the created resource object.
          <i>ppvResource</i> can be NULL, to enable capability testing. When <i>ppvResource</i> is NULL, no object will be created and S_FALSE will be returned when <i>pResourceDesc</i> is valid. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the resource.
            For other possible return values, see <a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
          




## -remarks



This method creates both a resource and a heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
          The created heap is known as an implicit heap, because the heap object cannot be obtained by the application.
          The application must ensure the GPU will no longer read or write to this resource before releasing the final reference on the resource.
        

The implicit heap is made resident for GPU access before the method returns to the application.
          See <a href="https://docs.microsoft.com/windows/desktop/direct3d12/residency">Residency</a>.
        

The resource GPU VA mapping cannot be changed.
          See
          <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">ID3D12CommandQueue::UpdateTileMappings</a>and
          <a href="https://docs.microsoft.com/windows/desktop/direct3d12/volume-tiled-resources">Volume Tiled Resources</a>.
        

This method may be called by multiple threads concurrently.
        


#### Examples

The <a href="https://docs.microsoft.com/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommittedResource</b> as follows:
        

Create a vertex buffer.


```cpp
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    IID_PPV_ARGS(&m_vertexBuffer)));

```


See <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
 

 

