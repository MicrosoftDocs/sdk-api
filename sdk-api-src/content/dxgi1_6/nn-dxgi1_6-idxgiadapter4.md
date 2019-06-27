---
UID: NN:dxgi1_6.IDXGIAdapter4
title: IDXGIAdapter4 (dxgi1_6.h)
author: windows-sdk-content
description: This interface represents a display subsystem, and extends this family of interfaces to expose a method to check for an adapter's compatibility with Arbitrary Code Guard (ACG).
old-location: direct3ddxgi\idxgiadapter4.htm
tech.root: direct3ddxgi
ms.assetid: 176958F9-94C8-4F80-B9A4-96BC9634292E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter4, IDXGIAdapter4 interface [DXGI], IDXGIAdapter4 interface [DXGI],described, direct3ddxgi.idxgiadapter4, dxgi1_6/IDXGIAdapter4
ms.topic: interface
f1_keywords: 
 - "dxgi1_6/IDXGIAdapter4"
req.header: dxgi1_6.h
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
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIAdapter4 interface


## -description


This interface represents a display subsystem, and extends this family of interfaces to expose a method to check for an adapter's compatibility with Arbitrary Code Guard (ACG).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>. <b>IDXGIAdapter4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgiadapter4-getdesc3">GetDesc3</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.6 description of an adapter or video card. This description includes information about ACG compatibility.

</td>
</tr>
</table> 


## -remarks



For more details, refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/residency">Residency</a> section of the D3D12 documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>
 

 

