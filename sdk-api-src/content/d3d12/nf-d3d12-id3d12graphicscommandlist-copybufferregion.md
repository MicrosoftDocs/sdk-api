---
UID: NF:d3d12.ID3D12GraphicsCommandList.CopyBufferRegion
title: ID3D12GraphicsCommandList::CopyBufferRegion
author: windows-sdk-content
description: Copies a region of a buffer from one resource to another.
old-location: direct3d12\id3d12graphicscommandlist_copybufferregion.htm
tech.root: direct3d12
ms.assetid: 46F89B85-EDAA-4095-B6C6-4CC47F972F09
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CopyBufferRegion, CopyBufferRegion method, CopyBufferRegion method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,CopyBufferRegion method, ID3D12GraphicsCommandList.CopyBufferRegion, ID3D12GraphicsCommandList::CopyBufferRegion, d3d12/ID3D12GraphicsCommandList::CopyBufferRegion, direct3d12.id3d12graphicscommandlist_copybufferregion
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
 - ID3D12GraphicsCommandList.CopyBufferRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::CopyBufferRegion


## -description


Copies a region of a buffer from one resource to another.
        


## -parameters




### -param pDstBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>

Specifies the destination <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>.
          


### -param DstOffset

Type: <b>UINT64</b>

Specifies a UINT64 offset (in bytes) into the destination resource.
          


### -param pSrcBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>

Specifies the source  <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>.
          


### -param SrcOffset

Type: <b>UINT64</b>

Specifies a UINT64 offset (in bytes) into the source resource, to start the copy from.
          


### -param NumBytes

Type: <b>UINT64</b>

Specifies the number of bytes to copy.
          


## -returns



This method does not return a value.
          




## -remarks



Consider using the <a href="https://msdn.microsoft.com/EFC305CF-FBA9-4192-999B-6C6BFCDFF51F">CopyResource</a> method when copying an entire resource, and use this method for copying regions of a resource.
        

<b>CopyBufferRegion</b> may be used to initialize resources which alias the same heap memory. See <a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a> for more details.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::CopyBufferRegion</b> as follows:
        


```cpp
inline UINT64 UpdateSubresources(
    _In_ ID3D12GraphicsCommandList* pCmdList,
    _In_ ID3D12Resource* pDestinationResource,
    _In_ ID3D12Resource* pIntermediate,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources,
    UINT64 RequiredSize,
    _In_reads_(NumSubresources) const D3D12_PLACED_SUBRESOURCE_FOOTPRINT* pLayouts,
    _In_reads_(NumSubresources) const UINT* pNumRows,
    _In_reads_(NumSubresources) const UINT64* pRowSizesInBytes,
    _In_reads_(NumSubresources) const D3D12_SUBRESOURCE_DATA* pSrcData)
{
    // Minor validation
    D3D12_RESOURCE_DESC IntermediateDesc = pIntermediate->GetDesc();
    D3D12_RESOURCE_DESC DestinationDesc = pDestinationResource->GetDesc();
    if (IntermediateDesc.Dimension != D3D12_RESOURCE_DIMENSION_BUFFER || 
        IntermediateDesc.Width < RequiredSize + pLayouts[0].Offset || 
        RequiredSize > (SIZE_T)-1 || 
        (DestinationDesc.Dimension == D3D12_RESOURCE_DIMENSION_BUFFER && 
            (FirstSubresource != 0 || NumSubresources != 1)))
    {
        return 0;
    }
    
    BYTE* pData;
    HRESULT hr = pIntermediate->Map(0, NULL, reinterpret_cast<void**>(&pData));
    if (FAILED(hr))
    {
        return 0;
    }
    
    for (UINT i = 0; i < NumSubresources; ++i)
    {
        if (pRowSizesInBytes[i] > (SIZE_T)-1) return 0;
        D3D12_MEMCPY_DEST DestData = { pData + pLayouts[i].Offset, pLayouts[i].Footprint.RowPitch, pLayouts[i].Footprint.RowPitch * pNumRows[i] };
        MemcpySubresource(&DestData, &pSrcData[i], (SIZE_T)pRowSizesInBytes[i], pNumRows[i], pLayouts[i].Footprint.Depth);
    }
    pIntermediate->Unmap(0, NULL);
    
    if (DestinationDesc.Dimension == D3D12_RESOURCE_DIMENSION_BUFFER)
    {
        CD3DX12_BOX SrcBox( UINT( pLayouts[0].Offset ), UINT( pLayouts[0].Offset + pLayouts[0].Footprint.Width ) );
        pCmdList->CopyBufferRegion(
            pDestinationResource, 0, pIntermediate, pLayouts[0].Offset, pLayouts[0].Footprint.Width);
    }
    else
    {
        for (UINT i = 0; i < NumSubresources; ++i)
        {
            CD3DX12_TEXTURE_COPY_LOCATION Dst(pDestinationResource, i + FirstSubresource);
            CD3DX12_TEXTURE_COPY_LOCATION Src(pIntermediate, pLayouts[i]);
            pCmdList->CopyTextureRegion(&Dst, 0, 0, 0, &Src, nullptr);
        }
    }
    return RequiredSize;
}

```


See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

