---
UID: NF:d3d11.ID3D11DeviceContext.Map
title: ID3D11DeviceContext::Map (d3d11.h)
description: Gets a pointer to the data contained in a subresource, and denies the GPU access to that subresource.
helpviewer_keywords: ["8c85eb6d-c7f1-0944-a729-628dc7dd5fbc","ID3D11DeviceContext interface [Direct3D 11]","Map method","ID3D11DeviceContext.Map","ID3D11DeviceContext::Map","Map","Map method [Direct3D 11]","Map method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::Map","direct3d11.id3d11devicecontext_map"]
old-location: direct3d11\id3d11devicecontext_map.htm
tech.root: direct3d11
ms.assetid: c9d57873-1faa-42fa-855c-26f565e3b27c
ms.date: 12/05/2018
ms.keywords: 8c85eb6d-c7f1-0944-a729-628dc7dd5fbc, ID3D11DeviceContext interface [Direct3D 11],Map method, ID3D11DeviceContext.Map, ID3D11DeviceContext::Map, Map, Map method [Direct3D 11], Map method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::Map, direct3d11.id3d11devicecontext_map
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::Map
 - d3d11/ID3D11DeviceContext::Map
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.Map
---

# ID3D11DeviceContext::Map


## -description

Gets a pointer to the data contained in a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-subresources">subresource</a>, and denies the GPU access to that subresource.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface.

### -param Subresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index number of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-subresources">subresource</a>.

### -param MapType [in]

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP</a></b>

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP</a>-typed value that specifies the CPU's read and write permissions for a resource.

### -param MapFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map_flag">Flag</a> that specifies what the CPU does when the GPU is busy. This flag is optional.

### -param pMappedResource [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_mapped_subresource">D3D11_MAPPED_SUBRESOURCE</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_mapped_subresource">D3D11_MAPPED_SUBRESOURCE</a> structure for the mapped subresource.
            See the Remarks section regarding NULL pointers.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.
            

This method also returns <b>DXGI_ERROR_WAS_STILL_DRAWING</b> if <i>MapFlags</i> specifies <b>D3D11_MAP_FLAG_DO_NOT_WAIT</b> and the GPU is not yet finished with the resource.
            

This method also returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if <i>MapType</i> allows any CPU read access and the video card has been removed.
            

For more information about these error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

If you call <b>Map</b> on a deferred context, you can only pass <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_DISCARD</a>, <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a>, or both to the <i>MapType</i> parameter. Other <b>D3D11_MAP</b>-typed values are not supported for a deferred context.
        

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.
        </div>
<div> </div>
For info about how to use <b>Map</b>, see <a href="/windows/desktop/direct3d11/how-to--use-dynamic-resources">How to: Use dynamic resources</a>.
      

<h3><a id="No_NULL_Pointers"></a><a id="no_null_pointers"></a><a id="NO_NULL_POINTERS"></a>NULL pointers for pMappedResource</h3>
The <i>pMappedResource</i> parameter may be NULL when a texture is provided that was created with
            <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a>,
            and the API is called on an immediate context.
            This allows a default texture to be mapped, even if it was created using
            <a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_texture_layout">D3D11_TEXTURE_LAYOUT_UNDEFINED</a>.
            Following this API call, the texture may be accessed using
            <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource">ID3D11DeviceContext3::WriteToSubresource</a> and/or
            <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource">ID3D11DeviceContext3::ReadFromSubresource</a>.
          

<h3><a id="No_Read_From_Write_Mapped"></a><a id="no_read_from_write_mapped"></a><a id="NO_READ_FROM_WRITE_MAPPED"></a>Don't read from a subresource mapped for writing</h3>
When you pass <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE</a>, <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_DISCARD</a>, or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a> to the <i>MapType</i> parameter, you must ensure that your app does not read the subresource data to which the <b>pData</b> member of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_mapped_subresource">D3D11_MAPPED_SUBRESOURCE</a> points because doing so can cause a significant performance penalty. The memory region to which <b>pData</b> points can be allocated with <a href="/windows/desktop/Memory/memory-protection-constants">PAGE_WRITECOMBINE</a>, and your app must honor all restrictions that are associated with such memory.<div class="alert"><b>Note</b>  <p class="note">Even the following C++ code can read from memory and trigger the performance penalty because the code can expand to the following x86 assembly code.
              

<p class="note">C++ code:
              


```
*((int*)MappedResource.pData) = 0;
```


<p class="note">x86 assembly code:
              


```
AND DWORD PTR [EAX],0
```


</div>
<div> </div>


Use the appropriate optimization settings and language constructs to help avoid this performance penalty. For example, you can avoid the xor optimization by using a <b>volatile</b> pointer or by optimizing for code speed instead of code size.
          

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>