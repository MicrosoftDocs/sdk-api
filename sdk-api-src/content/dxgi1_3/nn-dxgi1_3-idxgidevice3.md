---
UID: NN:dxgi1_3.IDXGIDevice3
title: IDXGIDevice3 (dxgi1_3.h)
author: windows-sdk-content
description: The IDXGIDevice3 interface implements a derived class for DXGI objects that produce image data. The interface exposes a method to trim graphics memory usage by the DXGI device.
old-location: direct3ddxgi\idxgidevice3.htm
tech.root: direct3ddxgi
ms.assetid: 3D6A0173-456D-4783-943D-35F335F358BE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIDevice3, IDXGIDevice3 interface [DXGI], IDXGIDevice3 interface [DXGI],described, direct3ddxgi.idxgidevice3, dxgi1_3/IDXGIDevice3
ms.topic: interface
f1_keywords: ["dxgi1_3/IDXGIDevice3"]
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDXGIDevice3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDevice3 interface


## -description


The <b>IDXGIDevice3</b> interface implements a derived class for DXGI objects that produce image data. The interface exposes a method to trim graphics memory usage by the DXGI device.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>. <b>IDXGIDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim">Trim</a>
</td>
<td align="left" width="63%">
Trims the graphics memory allocated by the <b>IDXGIDevice3</b>
DXGI device on the app's behalf.

</td>
</tr>
</table> 


## -remarks



The <b>IDXGIDevice3</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice3</b> interface. To retrieve the <b>IDXGIDevice3</b>  interface of a Direct3D device, use the following code:
        


```cpp
IDXGIDevice3 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice3), (void **)&pDXGIDevice);
```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>
 

 

