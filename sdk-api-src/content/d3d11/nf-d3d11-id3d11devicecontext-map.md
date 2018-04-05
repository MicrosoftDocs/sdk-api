---
UID: NF:d3d11.ID3D11DeviceContext.Map
title: ID3D11DeviceContext::Map method
author: windows-driver-content
description: Gets a pointer to the data contained in a subresource, and denies the GPU access to that subresource.
old-location: direct3d11\id3d11devicecontext_map.htm
old-project: direct3d11
ms.assetid: c9d57873-1faa-42fa-855c-26f565e3b27c
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 8c85eb6d-c7f1-0944-a729-628dc7dd5fbc, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], Map method, ID3D11DeviceContext::Map, Map method [Direct3D 11], Map method [Direct3D 11], ID3D11DeviceContext interface, Map,ID3D11DeviceContext.Map, d3d11/ID3D11DeviceContext::Map, direct3d11.id3d11devicecontext_map
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.Map
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::Map method


## -description



      Gets a pointer to the data contained in a <a href="https://msdn.microsoft.com/57444cb5-6c8b-4dac-8d6b-ca2b45eafac9">subresource</a>, and denies the GPU access to that subresource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface.
          


### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Index number of the <a href="https://msdn.microsoft.com/57444cb5-6c8b-4dac-8d6b-ca2b45eafac9">subresource</a>.
          


### -param MapType [in]

Type: <b><a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP</a></b>


            A <a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP</a>-typed value that specifies the CPU's read and write permissions for a resource.
          


### -param MapFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/986400c4-2a81-4d43-9564-d26eeaf7bd28">Flag</a> that specifies what the CPU does when the GPU is busy. This flag is optional.
          


### -param pMappedResource [out, optional]

Type: <b><a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a>*</b>


            A pointer to the <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a> structure for the mapped subresource.
            See the Remarks section regarding NULL pointers.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
            


              This method also returns <b>DXGI_ERROR_WAS_STILL_DRAWING</b> if <i>MapFlags</i> specifies <b>D3D11_MAP_FLAG_DO_NOT_WAIT</b> and the GPU is not yet finished with the resource.
            


              This method also returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if <i>MapType</i> allows any CPU read access and the video card has been removed.
            


              For more information about these error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.
            




## -remarks




          If you call <b>Map</b> on a deferred context, you can only pass <a href="d3d11_map.htm">D3D11_MAP_WRITE_DISCARD</a>, <a href="d3d11_map.htm">D3D11_MAP_WRITE_NO_OVERWRITE</a>, or both to the <i>MapType</i> parameter. Other <b>D3D11_MAP</b>-typed values are not supported for a deferred context.
        

<div class="alert"><b>Note</b>  
          The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="d3d11_map.htm">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> with <a href="d3d11_feature.htm">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.
        </div>
<div> </div>

        For info about how to use <b>Map</b>, see <a href="https://msdn.microsoft.com/E73EA4B0-BD14-430C-89CA-4CFCF92C7548">How to: Use dynamic resources</a>.
      

<h3><a id="No_NULL_Pointers"></a><a id="no_null_pointers"></a><a id="NO_NULL_POINTERS"></a>NULL pointers for pMappedResource</h3>

            The <i>pMappedResource</i> parameter may be NULL when a texture is provided that was created with
            <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a>,
            and the API is called on an immediate context.
            This allows a default texture to be mapped, even if it was created using
            <a href="https://msdn.microsoft.com/E7786550-99FC-4F8E-B93F-C2877C052EC2">D3D11_TEXTURE_LAYOUT_UNDEFINED</a>.
            Following this API call, the texture may be accessed using
            <a href="https://msdn.microsoft.com/DCA4A88D-3DCA-41D5-AE52-061A605A9CBF">ID3D11DeviceContext3::WriteToSubresource</a>
            and/or
            <a href="https://msdn.microsoft.com/060B9627-3A95-4DBD-B3E6-3989D8D9C79E">ID3D11DeviceContext3::ReadFromSubresource</a>.
          

<h3><a id="No_Read_From_Write_Mapped"></a><a id="no_read_from_write_mapped"></a><a id="NO_READ_FROM_WRITE_MAPPED"></a>Don't read from a subresource mapped for writing</h3>

            When you pass <a href="d3d11_map.htm">D3D11_MAP_WRITE</a>, <a href="d3d11_map.htm">D3D11_MAP_WRITE_DISCARD</a>, or <a href="d3d11_map.htm">D3D11_MAP_WRITE_NO_OVERWRITE</a> to the <i>MapType</i> parameter, you must ensure that your app does not read the subresource data to which the <b>pData</b> member of <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a> points because doing so can cause a significant performance penalty. The memory region to which <b>pData</b> points can be allocated with <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">PAGE_WRITECOMBINE</a>, and your app must honor all restrictions that are associated with such memory.<div class="alert"><b>Note</b>  <p class="note">
                Even the following C++ code can read from memory and trigger the performance penalty because the code can expand to the following x86 assembly code.
              

<p class="note">
                C++ code:
              

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>*((int*)MappedResource.pData) = 0;</pre>
</td>
</tr>
</table></span></div>
<p class="note">
                x86 assembly code:
              

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>AND DWORD PTR [EAX],0</pre>
</td>
</tr>
</table></span></div>
</div>
<div> </div>



            Use the appropriate optimization settings and language constructs to help avoid this performance penalty. For example, you can avoid the xor optimization by using a <b>volatile</b> pointer or by optimizing for code speed instead of code size.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

