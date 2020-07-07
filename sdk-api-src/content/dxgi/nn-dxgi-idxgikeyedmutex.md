---
UID: NN:dxgi.IDXGIKeyedMutex
title: IDXGIKeyedMutex (dxgi.h)
description: Represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.
helpviewer_keywords: ["624ec55f-8325-5294-526a-89138f1d7331","IDXGIKeyedMutex","IDXGIKeyedMutex interface [DXGI]","IDXGIKeyedMutex interface [DXGI]","described","direct3ddxgi.idxgikeyedmutex","dxgi/IDXGIKeyedMutex"]
old-location: direct3ddxgi\idxgikeyedmutex.htm
tech.root: direct3ddxgi
ms.assetid: f790eb46-f116-4258-8c8d-de1ece4a1f21
ms.date: 12/05/2018
ms.keywords: 624ec55f-8325-5294-526a-89138f1d7331, IDXGIKeyedMutex, IDXGIKeyedMutex interface [DXGI], IDXGIKeyedMutex interface [DXGI],described, direct3ddxgi.idxgikeyedmutex, dxgi/IDXGIKeyedMutex
f1_keywords:
- dxgi/IDXGIKeyedMutex
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
- IDXGIKeyedMutex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIKeyedMutex interface


## -description


Represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIKeyedMutex</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>. <b>IDXGIKeyedMutex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIKeyedMutex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-acquiresync">AcquireSync</a>
</td>
<td align="left" width="63%">
Using a key, acquires exclusive rendering access to a shared resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-releasesync">ReleaseSync</a>
</td>
<td align="left" width="63%">
Using a key, releases exclusive rendering access to a shared resource.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a> is required to create a resource capable of supporting the <b>IDXGIKeyedMutex</b> interface.

An <b>IDXGIKeyedMutex</b> should be retrieved for each device sharing a resource. In Direct3D 10.1, such a resource that is shared between two or more devices is created with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX</a>  flag. In Direct3D 11, such a resource that is shared between two or more devices is created with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX</a>  flag.

For information about creating a keyed mutex, see the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-acquiresync">IDXGIKeyedMutex::AcquireSync</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>
 

 

