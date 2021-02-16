---
UID: NF:d3d11.ID3D11DeviceContext.OMSetRenderTargetsAndUnorderedAccessViews
title: ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews (d3d11.h)
description: Binds resources to the output-merger stage.
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","OMSetRenderTargetsAndUnorderedAccessViews method","ID3D11DeviceContext.OMSetRenderTargetsAndUnorderedAccessViews","ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews","OMSetRenderTargetsAndUnorderedAccessViews","OMSetRenderTargetsAndUnorderedAccessViews method [Direct3D 11]","OMSetRenderTargetsAndUnorderedAccessViews method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews","direct3d11.id3d11devicecontext_omsetrendertargetsandunorderedaccessviews","ee2c41c6-fd01-a895-a163-330e4363a9d7"]
old-location: direct3d11\id3d11devicecontext_omsetrendertargetsandunorderedaccessviews.htm
tech.root: direct3d11
ms.assetid: 1973d40f-f0d0-497e-be7b-6cf55f8a7da2
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMSetRenderTargetsAndUnorderedAccessViews method, ID3D11DeviceContext.OMSetRenderTargetsAndUnorderedAccessViews, ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews, OMSetRenderTargetsAndUnorderedAccessViews, OMSetRenderTargetsAndUnorderedAccessViews method [Direct3D 11], OMSetRenderTargetsAndUnorderedAccessViews method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews, direct3d11.id3d11devicecontext_omsetrendertargetsandunorderedaccessviews, ee2c41c6-fd01-a895-a163-330e4363a9d7
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
 - ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews
 - d3d11/ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews
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
 - ID3D11DeviceContext.OMSetRenderTargetsAndUnorderedAccessViews
---

# ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews


## -description

Binds resources to the output-merger stage.

## -parameters

### -param NumRTVs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of render targets to bind (ranges between 0 and <b>D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT</b>). If this parameter is nonzero, the number of entries in the array to which <i>ppRenderTargetViews</i> points must equal the number in this parameter. If you set <i>NumRTVs</i> to D3D11_KEEP_RENDER_TARGETS_AND_DEPTH_STENCIL (0xffffffff), this method does not modify the currently bound render-target views (RTVs) and also does not modify depth-stencil view (DSV).

### -param ppRenderTargetViews [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>s that represent the render targets to bind to the device.
            If this parameter is <b>NULL</b> and <i>NumRTVs</i> is 0, no render targets are bound.

### -param pDepthStencilView [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a> that represents the depth-stencil view to bind to the device.
            If this parameter is <b>NULL</b>, the depth-stencil view is not bound.

### -param UAVStartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into a zero-based array to begin setting unordered-access views (ranges from 0 to D3D11_PS_CS_UAV_REGISTER_COUNT - 1).

For the Direct3D 11.1 runtime, which is available starting with Windows 8, this value can range from 0 to D3D11_1_UAV_SLOT_COUNT - 1. D3D11_1_UAV_SLOT_COUNT is defined as 64.
            

For pixel shaders, <i>UAVStartSlot</i> should be equal to the number of render-target views being bound.

### -param NumUAVs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of unordered-access views (UAVs) in <i>ppUnorderedAccessViews</i>. If you set <i>NumUAVs</i> to D3D11_KEEP_UNORDERED_ACCESS_VIEWS (0xffffffff), this method does not modify the currently bound unordered-access views.
            

For the Direct3D 11.1 runtime, which is available starting with Windows 8, this value can range from 0 to D3D11_1_UAV_SLOT_COUNT - <i>UAVStartSlot</i>.

### -param ppUnorderedAccessViews [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>s that represent the unordered-access views to bind to the device.
            If this parameter is <b>NULL</b> and <i>NumUAVs</i> is 0, no unordered-access views are bound.

### -param pUAVInitialCounts [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of append and consume buffer offsets. A value of -1 indicates to keep the current offset. Any other values set the hidden counter
            for that appendable and consumable UAV. <i>pUAVInitialCounts</i> is  relevant only for UAVs that were created with either
            <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag">D3D11_BUFFER_UAV_FLAG_APPEND</a> or <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> specified
            when the UAV was created; otherwise, the argument is ignored.

## -remarks

For pixel shaders, the render targets and unordered-access views share the same resource slots when being written out. This means that UAVs must be
          given an offset so that they are placed in the slots after the render target views that are being bound.
        

<div class="alert"><b>Note</b>  RTVs, DSV, and UAVs cannot be set independently; they all need to be set at the same time.</div>
<div> </div>
Two RTVs conflict if they share a subresource (and therefore share the same resource).

Two UAVs conflict if they share a subresource (and therefore share the same resource).

An RTV conflicts with a UAV if they share a subresource or share a bind point.

<b>OMSetRenderTargetsAndUnorderedAccessViews</b> operates properly in the following situations:
          

<ol>
<li>
<i>NumRTVs</i> != D3D11_KEEP_RENDER_TARGETS_AND_DEPTH_STENCIL and <i>NumUAVs</i> != D3D11_KEEP_UNORDERED_ACCESS_VIEWS
                

The following conditions must be true for <b>OMSetRenderTargetsAndUnorderedAccessViews</b> to succeed and for the runtime to pass the bind information to the driver:
                

<ul>
<li><i>NumRTVs</i> &lt;= 8
              </li>
<li><i>UAVStartSlot</i> &gt;= <i>NumRTVs</i></li>
<li><i>UAVStartSlot</i> + <i>NumUAVs</i> &lt;= 8
              </li>
<li>There must be no conflicts in the set of all <i>ppRenderTargetViews</i> and <i>ppUnorderedAccessViews</i>.
              </li>
<li><i>ppDepthStencilView</i> must match the render-target views. For more information about resource views, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Introduction to a Resource in Direct3D 11</a>.
              </li>
</ul>
<b>OMSetRenderTargetsAndUnorderedAccessViews</b> performs the following tasks:
              

<ul>
<li>Unbinds all currently bound conflicting resources (stream-output target resources (SOTargets), compute shader (CS) UAVs, shader-resource views (SRVs)).</li>
<li>Binds <i>ppRenderTargetViews</i>, <i>ppDepthStencilView</i>, and <i>ppUnorderedAccessViews</i>.
              </li>
</ul>
</li>
<li>
<i>NumRTVs</i> == D3D11_KEEP_RENDER_TARGETS_AND_DEPTH_STENCIL
                

In this situation, <b>OMSetRenderTargetsAndUnorderedAccessViews</b> binds only UAVs.
                

The following conditions must be true for <b>OMSetRenderTargetsAndUnorderedAccessViews</b> to succeed and for the runtime to pass the bind information to the driver:
                

<ul>
<li><i>UAVStartSlot</i> + <i>NumUAVs</i> &lt;= 8
              </li>
<li>There must be no conflicts in <i>ppUnorderedAccessViews</i>.
              </li>
</ul>
<b>OMSetRenderTargetsAndUnorderedAccessViews</b> unbinds the following items:
              

<ul>
<li>All RTVs in slots &gt;= <i>UAVStartSlot</i></li>
<li>All RTVs that conflict with any UAVs in <i>ppUnorderedAccessViews</i></li>
<li>All currently bound resources (SOTargets, CS UAVs, SRVs) that conflict with <i>ppUnorderedAccessViews</i></li>
</ul>
<b>OMSetRenderTargetsAndUnorderedAccessViews</b> binds <i>ppUnorderedAccessViews</i>.
            

<b>OMSetRenderTargetsAndUnorderedAccessViews</b> ignores <i>ppDepthStencilView</i>, and the current depth-stencil view remains bound.
            

</li>
<li>
<i>NumUAVs</i> == D3D11_KEEP_UNORDERED_ACCESS_VIEWS
                

In this situation, <b>OMSetRenderTargetsAndUnorderedAccessViews</b> binds only RTVs and DSV.
                

The following conditions must be true for <b>OMSetRenderTargetsAndUnorderedAccessViews</b> to succeed and for the runtime to pass the bind information to the driver:
                

<ul>
<li><i>NumRTVs</i> &lt;= 8
              </li>
<li>There must be no conflicts in <i>ppRenderTargetViews</i>.
              </li>
<li><i>ppDepthStencilView</i> must match the render-target views. For more information about resource views, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Introduction to a Resource in Direct3D 11</a>.
              </li>
</ul>
<b>OMSetRenderTargetsAndUnorderedAccessViews</b> unbinds the following items:
              

<ul>
<li>All UAVs in slots &lt; <i>NumRTVs</i></li>
<li>All UAVs that conflict with any RTVs in <i>ppRenderTargetViews</i></li>
<li>All currently bound resources (SOTargets, CS UAVs, SRVs) that conflict with <i>ppRenderTargetViews</i></li>
</ul>
<b>OMSetRenderTargetsAndUnorderedAccessViews</b> binds <i>ppRenderTargetViews</i> and <i>ppDepthStencilView</i>.
            

<b>OMSetRenderTargetsAndUnorderedAccessViews</b> ignores <i>UAVStartSlot</i>.
            

</li>
</ol>
<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>