---
UID: NN:dxgi.IDXGIDevice
title: IDXGIDevice (dxgi.h)
author: windows-sdk-content
description: An IDXGIDevice interface implements a derived class for DXGI objects that produce image data.
old-location: direct3ddxgi\idxgidevice.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 99cdbe06-c52d-a562-8d0a-c42fe333f947, IDXGIDevice, IDXGIDevice interface [DXGI], IDXGIDevice interface [DXGI],described, direct3ddxgi.idxgidevice, dxgi/IDXGIDevice
ms.topic: interface
f1_keywords: 
 - "dxgi/IDXGIDevice"
dev_langs:
 - c++
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDevice interface


## -description


An <b>IDXGIDevice</b> interface implements a derived class for DXGI objects that produce image data.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-createsurface">CreateSurface</a>
</td>
<td align="left" width="63%">
Returns a surface. This method is used internally and you should not call it directly in your application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter">GetAdapter</a>
</td>
<td align="left" width="63%">
Returns the adapter for the specified device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getgputhreadpriority">GetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Gets the GPU thread priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-queryresourceresidency">QueryResourceResidency</a>
</td>
<td align="left" width="63%">
Gets the residency status of an array of resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-setgputhreadpriority">SetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Sets the GPU thread priority.

</td>
</tr>
</table> 


## -remarks



The <b>IDXGIDevice</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice</b> interface. To retrieve the <b>IDXGIDevice</b>  interface of a Direct3D device, use the following code:
        


```
IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);

```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
 

 

