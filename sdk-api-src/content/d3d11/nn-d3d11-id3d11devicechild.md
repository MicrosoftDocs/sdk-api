---
UID: NN:d3d11.ID3D11DeviceChild
title: ID3D11DeviceChild
author: windows-sdk-content
description: A device-child interface accesses data used by a device.
old-location: direct3d11\id3d11devicechild.htm
old-project: direct3d11
ms.assetid: bed17239-0358-4768-8655-9a1d92f25a2e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceChild, ID3D11DeviceChild interface [Direct3D 11], ID3D11DeviceChild interface [Direct3D 11],described, d3d11/ID3D11DeviceChild, direct3d11.id3d11devicechild, ea2a7e4d-06b6-a8d0-51ff-52cc4806e595
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceChild
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceChild interface


## -description


A device-child interface accesses data used by a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceChild</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11DeviceChild</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceChild</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Get a pointer to the device that created this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11729527-680e-4c70-a10f-278feab8362d">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get application-defined data from a device child.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5d4c2f-fe1f-4131-9c04-2ea8fae6ee21">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set application-defined data to a device child and associate that data with an application-defined guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18b7daa3-a727-474d-836e-f47a56d39c89">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.

</td>
</tr>
</table> 


## -remarks



There are several types of device child interfaces, all of which inherit this interface. They include shaders, state objects, and input layouts.

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

