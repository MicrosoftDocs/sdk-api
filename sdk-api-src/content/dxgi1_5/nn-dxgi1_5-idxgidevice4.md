---
UID: NN:dxgi1_5.IDXGIDevice4
title: IDXGIDevice4
author: windows-sdk-content
description: This interface provides updated methods to offer and reclaim resources.
old-location: direct3ddxgi\idxgidevice4.htm
old-project: direct3ddxgi
ms.assetid: 15EA6B68-587E-4D92-A70D-7DDA9915EBC2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDXGIDevice4, IDXGIDevice4 interface [DXGI], IDXGIDevice4 interface [DXGI],described, direct3ddxgi.idxgidevice4, dxgi1_5/IDXGIDevice4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_5.h
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
req.typenames: DXGI_RECLAIM_RESOURCE_RESULTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIDevice4
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice4 interface


## -description


This interface provides updated methods to offer and reclaim resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice4</b> interface inherits from <a href="https://msdn.microsoft.com/3D6A0173-456D-4783-943D-35F335F358BE">IDXGIDevice3</a>. <b>IDXGIDevice4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7F6782F3-7779-4DBD-AD5A-AE0FB136FC70">OfferResources1</a>
</td>
<td align="left" width="63%">
Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83D09C41-CB96-4ADA-AE38-7D9542CCCFE0">ReclaimResources1</a>
</td>
<td align="left" width="63%">
Restores access to resources that were previously offered by calling <a href="https://msdn.microsoft.com/7F6782F3-7779-4DBD-AD5A-AE0FB136FC70">IDXGIDevice4::OfferResources1</a>.

</td>
</tr>
</table> 


## -remarks



The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice4</b> interface. To retrieve the <b>IDXGIDevice4</b>  interface of a Direct3D device, use the following code:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IDXGIDevice4 * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice4), (void **)&amp;pDXGIDevice);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>



<a href="https://msdn.microsoft.com/3D6A0173-456D-4783-943D-35F335F358BE">IDXGIDevice3</a>
 

 

