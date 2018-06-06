---
UID: NF:d3d12.ID3D12Device.CreateUnorderedAccessView
title: ID3D12Device::CreateUnorderedAccessView
author: windows-sdk-content
description: Creates a view for unordered accessing.
old-location: direct3d12\id3d12device_createunorderedaccessview.htm
old-project: direct3d12
ms.assetid: E834E469-2958-44A9-978F-F42D6BB6B1DC
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: CreateUnorderedAccessView, CreateUnorderedAccessView method, CreateUnorderedAccessView method,ID3D12Device interface, ID3D12Device interface,CreateUnorderedAccessView method, ID3D12Device.CreateUnorderedAccessView, ID3D12Device::CreateUnorderedAccessView, d3d12/ID3D12Device::CreateUnorderedAccessView, direct3d12.id3d12device_createunorderedaccessview
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
 - ID3D12Device.CreateUnorderedAccessView
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateUnorderedAccessView


## -description



          Creates a view for unordered accessing.
        


## -parameters




### -param pResource [in, optional]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> object that represents the unordered access.
          

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.



### -param pCounterResource [in, optional]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>


              The <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> for the counter (if any) associated with the UAV.
            


              If <i>pCounterResource</i> is not specified, the <b>CounterOffsetInBytes</b> member of the <a href="https://msdn.microsoft.com/13E48B8F-4EF7-45B7-88F2-61D9BA1801D2">D3D12_BUFFER_UAV</a> structure must be 0.
            


              If <i>pCounterResource</i> is specified, then there is a counter associated with the UAV, and the runtime performs validation of the following requirements:
            

<ul>
<li>
               The <b>StructureByteStride</b> member of the <a href="https://msdn.microsoft.com/13E48B8F-4EF7-45B7-88F2-61D9BA1801D2">D3D12_BUFFER_UAV</a> structure must be greater than 0.
              </li>
<li>
                The format must be DXGI_FORMAT_UNKNOWN.
              </li>
<li>
                The D3D12_BUFFER_UAV_FLAG_RAW flag (a <a href="https://msdn.microsoft.com/D5350B5B-4E15-4B9F-B3E0-5A3B1592ED5C">D3D12_BUFFER_UAV_FLAGS</a> enumeration constant) must not be set.
              </li>
<li>
                Both of the resources (<i>pResource</i> and <i>pCounterResource</i>) must be buffers.
              </li>
<li>
                The <b>CounterOffsetInBytes</b> member of the <a href="https://msdn.microsoft.com/13E48B8F-4EF7-45B7-88F2-61D9BA1801D2">D3D12_BUFFER_UAV</a> structure must be a multiple of 4 bytes, and must be within the range of the counter resource.
              </li>
<li><i>pResource</i> cannot be NULL
              </li>
<li><i>pDesc</i> cannot be NULL.
              </li>
</ul>

### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0C3A31FE-625D-4CB3-87FD-D2C33D008DD4">D3D12_UNORDERED_ACCESS_VIEW_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/0C3A31FE-625D-4CB3-87FD-D2C33D008DD4">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure that describes the unordered-access view.
          

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and for buffers UAVs target a full buffer and are typed, and for textures UAVs target the first mip and all array slices. Not all resources support null descriptor initialization.


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the unordered-access view.
          


## -returns




            Returns nothing.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

