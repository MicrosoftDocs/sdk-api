---
UID: NS:d3d11.D3D11_MAPPED_SUBRESOURCE
title: D3D11_MAPPED_SUBRESOURCE
author: windows-sdk-content
description: Provides access to subresource data.
old-location: direct3d11\d3d11_mapped_subresource.htm
tech.root: direct3d11
ms.assetid: cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 6581ca11-abcb-9ae4-0972-0f8f36933283, D3D11_MAPPED_SUBRESOURCE, D3D11_MAPPED_SUBRESOURCE structure [Direct3D 11], d3d11/D3D11_MAPPED_SUBRESOURCE, direct3d11.d3d11_mapped_subresource
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_MAPPED_SUBRESOURCE
product: Windows
targetos: Windows
req.typenames: D3D11_MAPPED_SUBRESOURCE
req.redist: 
---

# D3D11_MAPPED_SUBRESOURCE structure


## -description


Provides access to subresource data.


## -struct-fields




### -field pData

Type: <b>void*</b>

Pointer to the data. When <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a> provides the pointer, the runtime ensures that the pointer has a specific alignment, depending on the following feature levels:

<ul>
<li>For <a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL_10_0</a> and higher, the pointer is aligned to 16 bytes.</li>
<li>For lower than <a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL_10_0</a>, the pointer is aligned to 4 bytes.</li>
</ul>

### -field RowPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The row pitch, or width, or physical size (in bytes) of the data.


### -field DepthPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The depth pitch, or width, or physical size (in bytes)of the data.


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a>.

The values in these members tell you how much data you can view:

<ul>
<li><b>pData</b> points to row 0 and depth slice 0.</li>
<li><b>RowPitch</b> contains the value that the runtime adds to <b>pData</b> to move from row to row,  where each row contains multiple pixels.</li>
<li><b>DepthPitch</b> contains the value that the runtime adds to <b>pData</b> to move from depth slice to depth slice,  where each depth slice contains multiple rows.</li>
</ul>
When <b>RowPitch</b> and <b>DepthPitch</b> are not appropriate for the resource type, the runtime might set their values to 0. So, don't use these values for anything other than iterating over rows and depth. Here are some examples:

<ul>
<li>For <a href="https://msdn.microsoft.com/7f552b9b-c5fb-4bc2-a7ae-61983379db38">Buffer</a> and <a href="https://msdn.microsoft.com/5f6fd0e4-a73e-4d13-b3a0-c884b7912581">Texture1D</a>, the runtime assigns values  that aren't 0 to <b>RowPitch</b> and <b>DepthPitch</b>. For example, if a <b>Buffer</b> contains 8 bytes, the runtime assigns values to <b>RowPitch</b> and <b>DepthPitch</b> that are greater than or equal to 8.</li>
<li>For <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a>, the runtime still assigns a value that isn't 0 to <b>DepthPitch</b>, assuming that the field isn't used.</li>
</ul>
<div class="alert"><b>Note</b>  The runtime might assign values to <b>RowPitch</b> and <b>DepthPitch</b> that are larger than anticipated because there might be padding between rows and depth.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

