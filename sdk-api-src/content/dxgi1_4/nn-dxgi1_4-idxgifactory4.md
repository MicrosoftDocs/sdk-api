---
UID: NN:dxgi1_4.IDXGIFactory4
title: IDXGIFactory4 (dxgi1_4.h)
description: Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects.
old-location: direct3ddxgi\idxgifactory4.htm
tech.root: direct3ddxgi
ms.assetid: 248CF7CF-BC7D-430F-9EA1-638A42AAC021
ms.date: 12/05/2018
ms.keywords: IDXGIFactory4, IDXGIFactory4 interface [DXGI], IDXGIFactory4 interface [DXGI],described, direct3ddxgi.idxgifactory4, dxgi1_4/IDXGIFactory4
f1_keywords:
- dxgi1_4/IDXGIFactory4
dev_langs:
- c++
req.header: dxgi1_4.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dxgi.lib
- Dxgi.dll
api_name:
- IDXGIFactory4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory4 interface


## -description


Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactory3">IDXGIFactory3</a>. <b>IDXGIFactory4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIFactory4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid">EnumAdapterByLuid</a>
</td>
<td align="left" width="63%">
Outputs the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> for the specified LUID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter">EnumWarpAdapter</a>
</td>
<td align="left" width="63%">
Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactory3">IDXGIFactory3</a>
 

 

