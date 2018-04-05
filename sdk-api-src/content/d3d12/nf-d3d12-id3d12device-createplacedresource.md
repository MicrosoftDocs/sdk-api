---
UID: NF:d3d12.ID3D12Device.CreatePlacedResource
title: ID3D12Device::CreatePlacedResource method
author: windows-driver-content
description: Creates a resource that is placed in a specific heap. Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
old-location: direct3d12\id3d12device_createplacedresource.htm
old-project: direct3d12
ms.assetid: 4581A82D-D2B6-4CAE-A336-07B8CF90A0BA
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreatePlacedResource method, CreatePlacedResource method, ID3D12Device interface, CreatePlacedResource,ID3D12Device.CreatePlacedResource, ID3D12Device, ID3D12Device interface, CreatePlacedResource method, ID3D12Device::CreatePlacedResource, d3d12/ID3D12Device::CreatePlacedResource, direct3d12.id3d12device_createplacedresource
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Device.CreatePlacedResource
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreatePlacedResource method


## -description



          Creates a resource that is placed in a specific heap.
          Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
        


## -parameters




### -param pHeap [in]

Type: <b><a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>*</b>


            A pointer to the <a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a> interface that represents the heap in which the resource is placed.
          


### -param HeapOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>


            The offset, in bytes, to the resource.
            The <i>HeapOffset</i> must be a multiple of the resource's alignment, and <i>HeapOffset</i> plus the resource size must be smaller than or equal to the heap size.
            <a href="https://msdn.microsoft.com/43467E09-835B-4DB9-B0A4-F75868DE4609">GetResourceAllocationInfo</a> must be used to understand the sizes of texture resources.
          


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure that describes the resource.
          


### -param InitialState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


              The initial state of the resource, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
            


              When a resource is created together with a D3D12_HEAP_TYPE_UPLOAD heap, <i>InitialState</i> must be D3D12_RESOURCE_STATE_GENERIC_READ.
              When a resource is created together with a D3D12_HEAP_TYPE_READBACK heap, <i>InitialState</i> must be D3D12_RESOURCE_STATE_COPY_DEST.
            


### -param pOptimizedClearValue [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/03B67F91-C150-4719-8C43-D04F51DC9C06">D3D12_CLEAR_VALUE</a>*</b>


              Specifies a <a href="https://msdn.microsoft.com/03B67F91-C150-4719-8C43-D04F51DC9C06">D3D12_CLEAR_VALUE</a> that describes the default value for a clear color.
            

<i>pOptimizedClearValue</i> specifies a value for which clear operations are most optimal.
              When the created resource is a texture with either the D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL flags, applications should choose the value that the clear operation will most commonly be called with.
              Clear operations can be called with other values, but those operations will not be as efficient as when the value matches the one passed into resource creation.
              <i>pOptimizedClearValue</i> must be NULL when used with D3D12_RESOURCE_DIMENSION_BUFFER.
            


### -param riid

Type: <b><b>REFIID</b></b>


              The globally unique identifier (<b>GUID</b>) for the resource interface.
              This is an input parameter.
            


              The <b>REFIID</b>, or <b>GUID</b>, of the interface to the resource can be obtained by using the __uuidof() macro.
              For example, __uuidof(<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a resource.
              Although <b>riid</b> is, most commonly, the GUID for <b>ID3D12Resource</b>, it may be any GUID for any interface. 
              If the resource object doesn't support the interface for this GUID, creation will fail with E_NOINTERFACE.
            


### -param ppvResource [out, optional]

Type: <b><b>void</b>**</b>


            A pointer to a memory block that receives a pointer to the resource.
            <i>ppvResource</i> can be NULL, to enable capability testing. 
            When <i>ppvResource</i> is NULL, no object will be created and S_FALSE will be returned when <i>pResourceDesc</i> and other parameters are valid.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the resource.
            See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
          




## -remarks



<b>CreatePlacedResource</b> is similar to fully mapping a reserved resource to an offset within a heap; but the virtual address space associated with a heap may be reused as well.
      


        Placed resources are lighter weight than committed resources to create and destroy, because no heap is created or destroyed during this operation. 
        However, placed resources enable an even lighter weight technique to reuse memory than resource creation and destruction: reuse through aliasing and aliasing barriers.
        Multiple placed resources may simultaneously overlap each other on the same heap, but only a single overlapping resource can be used at a time.
      


        There are two placed resource usage semantics, a simple model and an advanced model.
        The simple model is recommended, and is the most likely model for tool support, until the advanced model is proven to be required by the app.
      

<h3><a id="Simple_Model"></a><a id="simple_model"></a><a id="SIMPLE_MODEL"></a>Simple Model</h3>

            Placed resources should be considered to be in one of two states: active or inactive.
            It is invalid for the GPU to either read or write from an inactive resource.
            Placed resources are created in the inactive state.
          


            Applications must activate a resource with an aliasing barrier on a command list, by passing the resource in <a href="https://msdn.microsoft.com/9855D609-E863-4334-B6BA-B6777FDAB82B">D3D12_RESOURCE_ALIASING_BARRIER</a>::<b>pResourceAfter</b>.
            <b>pResourceBefore</b> can be left NULL during an activation.
            All resources that share physical memory with the activated resource now become inactive or somewhat inactive, which includes overlapping placed and reserved resources.
            The amount of inactivation varies based on resource properties.
            Textures with undefined memory layouts are the worst case, as the entire texture must be inactivated atomically.
            For two overlapping resources with defined layouts, inactivation can result in only the overlapping aligned regions of a resource.
            Data inheritance can even be well-defined.
            For more details, see <a href="https://msdn.microsoft.com/53C5804B-0F81-41AF-83D2-A96DCDFDC94A">Memory Aliasing and Data Inheritance</a>.
            Aliasing barriers should be grouped up and submitted together, in order to maximize efficiency.
          


            After activation, resources with either the render target or depth stencil flags must be further initialized. See the notes on the required resource initialization below.

<h3><a id="Advanced_Model"></a><a id="advanced_model"></a><a id="ADVANCED_MODEL"></a>Advanced Model</h3>
The active/ inactive abstraction can be ignored and the following lower-level rules must be honored, instead: 

<ul>
<li>An aliasing barrier must be between two different GPU resource accesses of the same physical memory, as long as those accesses are within the same <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandLists</a> call.</li>
<li>The first rendering operation to certain types of aliased resource must still be an initialization, just like the Simple Model.</li>
</ul>
<h3><a id="Notes_on_the_aliasing_barrier"></a><a id="notes_on_the_aliasing_barrier"></a><a id="NOTES_ON_THE_ALIASING_BARRIER"></a>Notes on the aliasing barrier</h3>
The aliasing barrier may set NULL for both <i>pResourceAfter</i> and <i>pResourceBefore</i>. The memory coherence definition of <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandLists</a> and an aliasing barrier are the same, such that two aliased accesses to the same physical memory need no aliasing barrier when the accesses are in two different <b>ExecuteCommandLists</b> invocations. 

For D3D12 advanced usage models, the synchronization definition of <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandLists</a> is equivalent to an aliasing barrier. Therefore, applications may either insert an aliasing barrier between reusing physical memory, or ensure the two aliased usages of physical memory occurs in two separate calls to <b>ExecuteCommandLists</b>. 

<h3><a id="Notes_on_the_required_resource_initialization"></a><a id="notes_on_the_required_resource_initialization"></a><a id="NOTES_ON_THE_REQUIRED_RESOURCE_INITIALIZATION"></a>Notes on the required resource initialization</h3>
While the active/ inactive abstraction can be ignored in the advanced model, certain resource types still require initialization. Resources with either the render target or depth stencil flags must be initialized with either a clear operation or a collection of full subresource copies. If an aliasing barrier was used to denote the transition between two aliased resources, the initialization must occur after the aliasing barrier. This initialization is still required whenever a resource would've been activated in the simple model.

Placed and reserved resources with either the render target or depth stencil flags must be initialized with one of the following operations before other operations are supported.
 
 


<ul>
<li>A <i>Clear</i> operation; for example <a href="https://msdn.microsoft.com/5AB13E36-A189-41B4-AEF8-B5C5831655DB">ClearRenderTargetView</a> or <a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ClearDepthStencilView</a>.
 </li>
<li>A <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">DiscardResource</a> operation.</li>
<li>A <i>Copy</i> operation; for example <a href="https://msdn.microsoft.com/46F89B85-EDAA-4095-B6C6-4CC47F972F09">CopyBufferRegion</a>, <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>, or <a href="https://msdn.microsoft.com/EFC305CF-FBA9-4192-999B-6C6BFCDFF51F">CopyResource</a>.</li>
</ul>
Applications should prefer the most explicit operation that results in the least amount of texels modified. Consider the following examples.
 
 

<ul>
<li>Using a depth buffer to solve pixel visibility typically requires each depth texel start out at 1.0 or 0. Therefore, a <i>Clear</i> operation should be the most efficient option for aliased depth buffer initialization.</li>
<li>An application may use an aliased render target as a destination for tone mapping. Since the application will render over every pixel during the tone mapping, <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">DiscardResource</a> should be the most efficient option for initialization.</li>
</ul>
 Initialization operations must either occur on an entire subresource or on a 64KB granularity. An entire subresource initialization is supported for all resource types. A 64KB initialization granularity, aligned at a 64KB offset, is supported for buffers and textures with either the 64KB_UNDEFINED_SWIZZLE or 64KB_STANDARD_SWIZZLE texture layout (refer to <a href="https://msdn.microsoft.com/1C61B658-9CA1-493C-8DBC-86313D0D302F">D3D12_TEXTURE_LAYOUT</a>).




## -see-also




<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">CreateCommittedResource</a>



<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">CreateReservedResource</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/67C6B1D4-BF76-45A9-BADC-7C9520C900EB">Shared Heaps</a>
 

 

