---
UID: NF:d3d12.ID3D12Device.CreateCommittedResource
title: ID3D12Device::CreateCommittedResource method
author: windows-driver-content
description: Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
old-location: direct3d12\id3d12device_createcommittedresource.htm
old-project: direct3d12
ms.assetid: FF9E8F11-F2C5-4A96-8E25-140870D15DA9
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: CreateCommittedResource method, CreateCommittedResource method, ID3D12Device interface, CreateCommittedResource,ID3D12Device.CreateCommittedResource, ID3D12Device, ID3D12Device interface, CreateCommittedResource method, ID3D12Device::CreateCommittedResource, d3d12/ID3D12Device::CreateCommittedResource, direct3d12.id3d12device_createcommittedresource
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
-	ID3D12Device.CreateCommittedResource
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateCommittedResource method


## -description



          Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
        


## -parameters




### -param pHeapProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure that provides properties for the resource's heap.
          


### -param HeapFlags

Type: <b><a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a></b>


            Heap options, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a> enumeration constants.
          


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure that describes the resource.
          


### -param InitialResourceState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


              The initial state of the resource, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
            


              When a resource is created together with a <a href="https://msdn.microsoft.com/5B1EA8A6-BD59-4B92-B6C4-A5C26D0B16D4">D3D12_HEAP_TYPE</a>_UPLOAD heap, <i>InitialResourceState</i> must be <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE</a>_GENERIC_READ.
              When a resource is created together with a D3D12_HEAP_TYPE_READBACK heap, <i>InitialResourceState</i> must be D3D12_RESOURCE_STATE_COPY_DEST.
            


### -param pOptimizedClearValue [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/03B67F91-C150-4719-8C43-D04F51DC9C06">D3D12_CLEAR_VALUE</a>*</b>


              Specifies a <a href="https://msdn.microsoft.com/03B67F91-C150-4719-8C43-D04F51DC9C06">D3D12_CLEAR_VALUE</a> that describes the default value for a clear color.
            

<i>pOptimizedClearValue</i> specifies a value for which clear operations are most optimal. When the created resource is a texture with either the <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAG</a>_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL flags, applications should choose the value that the clear operation will most commonly be called with. Clear operations can be called with other values, but those operations will not be as efficient as when the value matches the one passed into resource creation.
              <i>pOptimizedClearValue</i> must be NULL when used with <a href="https://msdn.microsoft.com/E04F3124-01FB-4EE7-BDF8-4821F2F1FCEB">D3D12_RESOURCE_DIMENSION</a>_BUFFER.
            


### -param riidResource

Type: <b><b>REFIID</b></b>


              The globally unique identifier (<b>GUID</b>) for the resource interface.
              This is an input parameter.
              The <b>REFIID</b>, or <b>GUID</b>, of the interface to the resource can be obtained by using the __uuidof() macro.
              For example, __uuidof(<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a resource.
            


              While riidResource is, most commonly, the GUID for <b>ID3D12Resource</b>, it may be any GUID for any interface.
              If the resource object doesn't support the interface for this GUID, creation will fail with E_NOINTERFACE.
            


### -param ppvResource [out, optional]

Type: <b><b>void</b>**</b>


            A pointer to memory that receives the requested interface pointer to the created resource object.
          <i>ppvResource</i> can be NULL, to enable capability testing. When <i>ppvResource</i> is NULL, no object will be created and S_FALSE will be returned when <i>pResourceDesc</i> is valid. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the resource.
            For other possible return values, see <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




          This method creates both a resource and a heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
          The created heap is known as an implicit heap, because the heap object cannot be obtained by the application.
          The application must ensure the GPU will no longer read or write to this resource before releasing the final reference on the resource.
        


          The implicit heap is made resident for GPU access before the method returns to the application.
          See <a href="https://msdn.microsoft.com/956F80D7-EEC8-4D88-B251-EE325614F31E">Residency</a>.
        


          The resource GPU VA mapping cannot be changed.
          See
          <a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">ID3D12CommandQueue::UpdateTileMappings</a>
          and
          <a href="https://msdn.microsoft.com/F670D15D-BC0F-4F90-99C1-A35192FE8980">Volume Tiled Resources</a>.
        


          This method may be called by multiple threads concurrently.
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommittedResource</b> as follows:
        

Create a vertex buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ThrowIfFailed(m_device-&gt;CreateCommittedResource(
    &amp;CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
    D3D12_HEAP_FLAG_NONE,
    &amp;CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    IID_PPV_ARGS(&amp;m_vertexBuffer)));
</pre>
</td>
</tr>
</table></span></div>

            See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a>



<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">CreateReservedResource</a>



<a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

