---
UID: NF:d3d12.ID3D12Device.GetCopyableFootprints
title: ID3D12Device::GetCopyableFootprints
author: windows-sdk-content
description: Gets a resource layout that can be copied. Helps the app fill-in D3D12_PLACED_SUBRESOURCE_FOOTPRINT and D3D12_SUBRESOURCE_FOOTPRINT when suballocating space in upload heaps.
old-location: direct3d12\id3d12device_getcopyablefootprints.htm
old-project: direct3d12
ms.assetid: EB3715A9-5A73-45DA-A46F-7889188409A3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetCopyableFootprints, GetCopyableFootprints method, GetCopyableFootprints method,ID3D12Device interface, ID3D12Device interface,GetCopyableFootprints method, ID3D12Device.GetCopyableFootprints, ID3D12Device::GetCopyableFootprints, d3d12/ID3D12Device::GetCopyableFootprints, direct3d12.id3d12device_getcopyablefootprints
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
 - d3d12.dll
api_name:
 - ID3D12Device.GetCopyableFootprints
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device::GetCopyableFootprints


## -description


Gets a resource layout that can be copied.
          Helps the app fill-in 
          <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and 
          <a href="https://msdn.microsoft.com/C73B6AB0-F9C5-432E-BA26-3B7772411C95">D3D12_SUBRESOURCE_FOOTPRINT</a> when suballocating space in upload heaps.
        


## -parameters




### -param pResourceDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a>*</b>

A description of the resource, as a pointer to a <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure.
          


### -param FirstSubresource [in]

Type: <b>UINT</b>

Index of the first subresource in the resource.
            The range of valid values is 0 to D3D12_REQ_SUBRESOURCES.
          


### -param NumSubresources [in]

Type: <b>UINT</b>

The number of subresources in the resource.  The range of valid values is 0 to (D3D12_REQ_SUBRESOURCES - <i>FirstSubresource</i>).
          


### -param BaseOffset

Type: <b>UINT64</b>

The offset, in bytes, to the resource.
          


### -param pLayouts [out, optional]

Type: <b><a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>*</b>

A pointer to an array (of length <i>NumSubresources</i>) of
            <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structures, to be filled with the description and placement of each subresource.
          


### -param pNumRows [out, optional]

Type: <b>UINT*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer  variables, to be filled with the number of rows for each subresource.
          


### -param pRowSizeInBytes [out, optional]

Type: <b>UINT64*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer variables, each entry to be filled with the unpadded size in bytes of a row, of each subresource.
          

For example, if a Texture2D resource has a width of 32 and bytes per pixel of 4, 

then <i>pRowSizeInBytes</i> returns 128.

<i>pRowSizeInBytes</i> should not be confused with <b>row pitch</b>, as examining <i>pLayouts</i> and getting the row pitch from that will give you 256 as it is aligned to D3D12_TEXTURE_DATA_PITCH_ALIGNMENT.


### -param pTotalBytes [out, optional]

Type: <b>UINT64*</b>

A pointer to an integer variable, to be filled with the total size, in bytes.
          


## -returns



This method does not return a value.
          




## -remarks



This routine assists the application in filling out
          <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and
          <a href="https://msdn.microsoft.com/C73B6AB0-F9C5-432E-BA26-3B7772411C95">D3D12_SUBRESOURCE_FOOTPRINT</a> structures, when suballocating space in upload heaps.
          The resulting structures are GPU adapter-agnostic, meaning that the values will not vary from one GPU adapter to the next.
          <b>GetCopyableFootprints</b> uses specified details about resource formats, texture layouts, and alignment requirements (from the <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> structure)  to fill out the subresource structures.
          Applications have access to all these details, so this method, or a variation of it, could be  written as part of the app.
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Multithreading</a> sample uses <b>ID3D12Device::GetCopyableFootprints</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource-&gt;GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource-&gt;GetDevice(__uuidof(*pDevice), reinterpret_cast&lt;void**&gt;(&amp;pDevice));
    pDevice-&gt;GetCopyableFootprints(&amp;Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &amp;RequiredSize);
    pDevice-&gt;Release();
    
    return RequiredSize;
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/F18D41BE-8AEF-444E-AC8B-EC57C63BF083">CD3DX12_RESOURCE_DESC</a>



<a href="https://msdn.microsoft.com/17266FB0-41B5-4A70-A896-206B54F5E76F">CD3DX12_SUBRESOURCE_FOOTPRINT</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

