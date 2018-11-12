---
UID: NF:d3d12.ID3D12Device.CreateReservedResource
title: ID3D12Device::CreateReservedResource
author: windows-sdk-content
description: Creates a resource that is reserved, which is not yet mapped to any pages in a heap.
old-location: direct3d12\id3d12device_createreservedresource.htm
tech.root: direct3d12
ms.assetid: 37E74129-1B5C-4997-A584-D7E9F92342EA
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateReservedResource, CreateReservedResource method, CreateReservedResource method,ID3D12Device interface, ID3D12Device interface,CreateReservedResource method, ID3D12Device.CreateReservedResource, ID3D12Device::CreateReservedResource, d3d12/ID3D12Device::CreateReservedResource, direct3d12.id3d12device_createreservedresource
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
 - ID3D12Device.CreateReservedResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateReservedResource


## -description


Creates a resource that is reserved, which is not yet mapped to any pages in a heap.
        


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure that describes the resource.
          


### -param InitialState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>

The initial state of the resource, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
            


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
              See Remarks.
              This is an input parameter.
            

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the resource can be obtained by using the __uuidof() macro.
              For example, __uuidof(<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a resource.
              Although <i>riid</i> is, most commonly, the GUID for <b>ID3D12Resource</b>, it may be any GUID for any interface.
              If the resource object doesn't support the interface for this GUID, creation will fail with E_NOINTERFACE.
            


### -param ppvResource [out, optional]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the resource.
            <i>ppvResource</i> can be NULL, to enable capability testing.
            When <i>ppvResource</i> is NULL, no object will be created and S_FALSE will be returned when <i>pDesc</i> is valid.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the resource.
            See <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a> for other possible return values.
          




## -remarks



<b>CreateReservedResource</b> is equivalent to D3D11_RESOURCE_MISC_TILED in D3D11.
        It creates a resource with virtual memory only, no backing store.
        The resource must be mapped to physical memory (that is, heaps) using <a href="https://msdn.microsoft.com/en-us/library/Dn788629(v=VS.85).aspx">CopyTileMappings</a> and <a href="https://msdn.microsoft.com/en-us/library/Dn788641(v=VS.85).aspx">UpdateTileMappings</a>.
      

These resource types can only be created when the adapter supports tiled resource tier 1 or greater.
        The tiled resource tier defines the behavior of accessing a resource that is not mapped to a heap.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn899178(v=VS.85).aspx">CreateCommittedResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899180(v=VS.85).aspx">CreatePlacedResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>
 

 

