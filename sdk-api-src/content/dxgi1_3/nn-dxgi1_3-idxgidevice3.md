---
UID: NN:dxgi1_3.IDXGIDevice3
title: IDXGIDevice3
author: windows-sdk-content
description: The IDXGIDevice3 interface implements a derived class for DXGI objects that produce image data. The interface exposes a method to trim graphics memory usage by the DXGI device.
old-location: direct3ddxgi\idxgidevice3.htm
tech.root: direct3ddxgi
ms.assetid: 3D6A0173-456D-4783-943D-35F335F358BE
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDXGIDevice3, IDXGIDevice3 interface [DXGI], IDXGIDevice3 interface [DXGI],described, direct3ddxgi.idxgidevice3, dxgi1_3/IDXGIDevice3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IDXGIDevice3 interface


## -description


The <b>IDXGIDevice3</b> interface implements a derived class for DXGI objects that produce image data. The interface exposes a method to trim graphics memory usage by the DXGI device.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>. <b>IDXGIDevice3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7A697B4B-4D0E-46F9-BC82-860FB91B365B">Trim</a>
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
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice3</b> interface. To retrieve the <b>IDXGIDevice3</b>  interface of a Direct3D device, use the following code:
        


```cpp
IDXGIDevice3 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice3), (void **)&pDXGIDevice);
```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>
 

 

