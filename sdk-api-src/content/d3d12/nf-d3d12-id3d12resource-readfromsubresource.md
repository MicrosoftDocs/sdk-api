---
UID: NF:d3d12.ID3D12Resource.ReadFromSubresource
title: ID3D12Resource::ReadFromSubresource
author: windows-sdk-content
description: Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts.
old-location: direct3d12\id3d12resource_readfromsubresource.htm
tech.root: direct3d12
ms.assetid: A1F61217-A383-49BF-B675-FBC7F6D015DB
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12Resource interface,ReadFromSubresource method, ID3D12Resource.ReadFromSubresource, ID3D12Resource::ReadFromSubresource, ReadFromSubresource, ReadFromSubresource method, ReadFromSubresource method,ID3D12Resource interface, d3d12/ID3D12Resource::ReadFromSubresource, direct3d12.id3d12resource_readfromsubresource
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Resource.ReadFromSubresource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Resource::ReadFromSubresource


## -description


Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts.
        


## -parameters




### -param pDstData [out]

Type: <b>void*</b>

A pointer to the destination data in memory.
          


### -param DstRowPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The distance from one row of destination data to the next row.
          


### -param DstDepthPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The distance from one depth slice of destination data to the next.
          


### -param SrcSubresource

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the index of the subresource to read from.
          


### -param pSrcBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/DD3973CC-043E-486E-9403-B46D8B7DE644">D3D12_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data from.
              If NULL, the data is read from the destination subresource with no offset.
              The dimensions of the destination must fit the destination (see
              <a href="https://msdn.microsoft.com/DD3973CC-043E-486E-9403-B46D8B7DE644">D3D12_BOX</a>).
            

An empty box results in a no-op.
              A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value.
              When the box is empty, this method doesn't perform any operation.
            


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



See the Remarks section for <a href="https://msdn.microsoft.com/8781E2FE-8D82-41F5-B541-A96DA11CA290">WriteToSubresource</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>



<a href="https://msdn.microsoft.com/C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F">Subresources</a>
 

 

