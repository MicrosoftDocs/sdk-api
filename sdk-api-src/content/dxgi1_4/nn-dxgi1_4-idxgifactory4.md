---
UID: NN:dxgi1_4.IDXGIFactory4
title: IDXGIFactory4
author: windows-sdk-content
description: Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects.
old-location: direct3ddxgi\idxgifactory4.htm
old-project: direct3ddxgi
ms.assetid: 248CF7CF-BC7D-430F-9EA1-638A42AAC021
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IDXGIFactory4, IDXGIFactory4 interface [DXGI], IDXGIFactory4 interface [DXGI],described, direct3ddxgi.idxgifactory4, dxgi1_4/IDXGIFactory4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory4 interface


## -description



          Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory4</b> interface inherits from <a href="https://msdn.microsoft.com/63B7A8E3-9A8F-409F-84DA-E9303C52A146">IDXGIFactory3</a>. <b>IDXGIFactory4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/AC800F32-2922-45BA-A6D3-D3E45113B9A7">EnumAdapterByLuid</a>
</td>
<td align="left" width="63%">

          Outputs the <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> for the specified LUID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18991B1A-5FA7-4298-A5FD-C8D7C485E4F7">EnumWarpAdapter</a>
</td>
<td align="left" width="63%">

          Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>



<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>



<a href="https://msdn.microsoft.com/63B7A8E3-9A8F-409F-84DA-E9303C52A146">IDXGIFactory3</a>
 

 

