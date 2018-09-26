---
UID: NN:dxgi.IDXGIDevice
title: IDXGIDevice
author: windows-sdk-content
description: An IDXGIDevice interface implements a derived class for DXGI objects that produce image data.
old-location: direct3ddxgi\idxgidevice.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 99cdbe06-c52d-a562-8d0a-c42fe333f947, IDXGIDevice, IDXGIDevice interface [DXGI], IDXGIDevice interface [DXGI],described, direct3ddxgi.idxgidevice, dxgi/IDXGIDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDevice interface


## -description


An <b>IDXGIDevice</b> interface implements a derived class for DXGI objects that produce image data.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice</b> interface inherits from <a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>. <b>IDXGIDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d0effc0a-0ec9-4350-ac44-c64c29984a02">CreateSurface</a>
</td>
<td align="left" width="63%">
Returns a surface. This method is used internally and you should not call it directly in your application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae113b36-47fd-4db1-b10c-ced22ec52435">GetAdapter</a>
</td>
<td align="left" width="63%">
Returns the adapter for the specified device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9e00d10-df95-4c89-89b3-e9c534bff933">GetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Gets the GPU thread priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">QueryResourceResidency</a>
</td>
<td align="left" width="63%">
Gets the residency status of an array of resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe140ee8-59d0-4285-b541-bedc6d3c3898">SetGPUThreadPriority</a>
</td>
<td align="left" width="63%">
Sets the GPU thread priority.

</td>
</tr>
</table> 


## -remarks



The <b>IDXGIDevice</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice</b> interface. To retrieve the <b>IDXGIDevice</b>  interface of a Direct3D device, use the following code:
        


```
IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);

```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

