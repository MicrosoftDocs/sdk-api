---
UID: NN:dxgi1_2.IDXGIDevice2
title: IDXGIDevice2
author: windows-sdk-content
description: The IDXGIDevice2 interface implements a derived class for DXGI objects that produce image data. The interface exposes methods to block CPU processing until the GPU completes processing, and to offer resources to the operating system.
old-location: direct3ddxgi\idxgidevice2.htm
old-project: direct3ddxgi
ms.assetid: 0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IDXGIDevice2, IDXGIDevice2 interface [DXGI], IDXGIDevice2 interface [DXGI],described, direct3ddxgi.idxgidevice2, dxgi1_2/IDXGIDevice2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDevice2
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice2 interface


## -description



        The <b>IDXGIDevice2</b> interface implements a derived class for DXGI objects that produce image data. The interface exposes methods to block CPU processing until the GPU completes processing, and to offer resources to the operating system.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice2</b> interface inherits from <a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>. <b>IDXGIDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CECF3ED6-A025-48C4-A7E2-971B86A262F0">EnqueueSetEvent</a>
</td>
<td align="left" width="63%">
Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">OfferResources</a>
</td>
<td align="left" width="63%">
Allows the operating system to free the video memory of resources by discarding their content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a>
</td>
<td align="left" width="63%">
Restores access to resources that were previously offered by calling <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a>.

</td>
</tr>
</table> 


## -remarks




          The <b>IDXGIDevice2</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        


          The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice2</b> interface. To retrieve the <b>IDXGIDevice2</b>  interface of a Direct3D device, use the following code:
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIDevice2 * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice2), (void **)&amp;pDXGIDevice);
</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>
 

 

