---
UID: NN:dxgi1_5.IDXGIDevice4
title: IDXGIDevice4 (dxgi1_5.h)

description: This interface provides updated methods to offer and reclaim resources.
old-location: direct3ddxgi\idxgidevice4.htm
tech.root: direct3ddxgi
ms.assetid: 15EA6B68-587E-4D92-A70D-7DDA9915EBC2

ms.date: 12/05/2018
ms.keywords: IDXGIDevice4, IDXGIDevice4 interface [DXGI], IDXGIDevice4 interface [DXGI],described, direct3ddxgi.idxgidevice4, dxgi1_5/IDXGIDevice4
ms.topic: interface
f1_keywords: 
 - "dxgi1_5/IDXGIDevice4"
dev_langs:
 - c++
req.header: dxgi1_5.h
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
 - IDXGIDevice4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDevice4 interface


## -description


This interface provides updated methods to offer and reclaim resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a>. <b>IDXGIDevice4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDevice4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1">OfferResources1</a>
</td>
<td align="left" width="63%">
Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1">ReclaimResources1</a>
</td>
<td align="left" width="63%">
Restores access to resources that were previously offered by calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1">IDXGIDevice4::OfferResources1</a>.

</td>
</tr>
</table> 


## -remarks



The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice4</b> interface. To retrieve the <b>IDXGIDevice4</b>  interface of a Direct3D device, use the following code:
        


```cpp
IDXGIDevice4 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice4), (void **)&pDXGIDevice);
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a>
 

 

