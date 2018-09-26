---
UID: NF:d3d12.ID3D12Device.CreateUnorderedAccessView
title: ID3D12Device::CreateUnorderedAccessView
author: windows-sdk-content
description: Creates a view for unordered accessing.
old-location: direct3d12\id3d12device_createunorderedaccessview.htm
tech.root: direct3d12
ms.assetid: E834E469-2958-44A9-978F-F42D6BB6B1DC
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CreateUnorderedAccessView, CreateUnorderedAccessView method, CreateUnorderedAccessView method,ID3D12Device interface, ID3D12Device interface,CreateUnorderedAccessView method, ID3D12Device.CreateUnorderedAccessView, ID3D12Device::CreateUnorderedAccessView, d3d12/ID3D12Device::CreateUnorderedAccessView, direct3d12.id3d12device_createunorderedaccessview
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
 - ID3D12Device.CreateUnorderedAccessView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateUnorderedAccessView


## -description


Creates a view for unordered accessing.
        


## -parameters




### -param pResource [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a> object that represents the unordered access.
          

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.



### -param pCounterResource [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>*</b>

The <a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a> for the counter (if any) associated with the UAV.
            

If <i>pCounterResource</i> is not specified, the <b>CounterOffsetInBytes</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn770345(v=VS.85).aspx">D3D12_BUFFER_UAV</a> structure must be 0.
            

If <i>pCounterResource</i> is specified, then there is a counter associated with the UAV, and the runtime performs validation of the following requirements:
            

<ul>
<li>The <b>StructureByteStride</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn770345(v=VS.85).aspx">D3D12_BUFFER_UAV</a> structure must be greater than 0.
              </li>
<li>The format must be DXGI_FORMAT_UNKNOWN.
              </li>
<li>The D3D12_BUFFER_UAV_FLAG_RAW flag (a <a href="https://msdn.microsoft.com/en-us/library/Dn986720(v=VS.85).aspx">D3D12_BUFFER_UAV_FLAGS</a> enumeration constant) must not be set.
              </li>
<li>Both of the resources (<i>pResource</i> and <i>pCounterResource</i>) must be buffers.
              </li>
<li>The <b>CounterOffsetInBytes</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dn770345(v=VS.85).aspx">D3D12_BUFFER_UAV</a> structure must be a multiple of 4 bytes, and must be within the range of the counter resource.
              </li>
<li><i>pResource</i> cannot be NULL
              </li>
<li><i>pDesc</i> cannot be NULL.
              </li>
</ul>

### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn770451(v=VS.85).aspx">D3D12_UNORDERED_ACCESS_VIEW_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn770451(v=VS.85).aspx">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure that describes the unordered-access view.
          

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and for buffers UAVs target a full buffer and are typed, and for textures UAVs target the first mip and all array slices. Not all resources support null descriptor initialization.


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn859369(v=VS.85).aspx">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the unordered-access view.
          


## -returns



Returns nothing.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>
 

 

