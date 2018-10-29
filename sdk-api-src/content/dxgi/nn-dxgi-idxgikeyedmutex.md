---
UID: NN:dxgi.IDXGIKeyedMutex
title: IDXGIKeyedMutex
author: windows-sdk-content
description: Represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.
old-location: direct3ddxgi\idxgikeyedmutex.htm
tech.root: direct3ddxgi
ms.assetid: f790eb46-f116-4258-8c8d-de1ece4a1f21
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 624ec55f-8325-5294-526a-89138f1d7331, IDXGIKeyedMutex, IDXGIKeyedMutex interface [DXGI], IDXGIKeyedMutex interface [DXGI],described, direct3ddxgi.idxgikeyedmutex, dxgi/IDXGIKeyedMutex
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
 - IDXGIKeyedMutex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIKeyedMutex interface


## -description


Represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIKeyedMutex</b> interface inherits from <a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>. <b>IDXGIKeyedMutex</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/31edab76-7b16-4a02-83ff-998c21e77f2e">AcquireSync</a>
</td>
<td align="left" width="63%">
Using a key, acquires exclusive rendering access to a shared resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/324741c9-33f2-4420-8c3f-4984e2ca0962">ReleaseSync</a>
</td>
<td align="left" width="63%">
Using a key, releases exclusive rendering access to a shared resource.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> is required to create a resource capable of supporting the <b>IDXGIKeyedMutex</b> interface.

An <b>IDXGIKeyedMutex</b> should be retrieved for each device sharing a resource. In Direct3D 10.1, such a resource that is shared between two or more devices is created with the <a href="https://msdn.microsoft.com/bdcb4e87-0285-4e96-a7ce-e08a43d3a4cb">D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX</a>  flag. In Direct3D 11, such a resource that is shared between two or more devices is created with the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX</a>  flag.

For information about creating a keyed mutex, see the <a href="https://msdn.microsoft.com/31edab76-7b16-4a02-83ff-998c21e77f2e">IDXGIKeyedMutex::AcquireSync</a> method.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>
 

 

