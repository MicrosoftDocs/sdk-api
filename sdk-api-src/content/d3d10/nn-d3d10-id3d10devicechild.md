---
UID: NN:d3d10.ID3D10DeviceChild
title: ID3D10DeviceChild
author: windows-sdk-content
description: A device-child interface accesses data used by a device.
old-location: direct3d10\id3d10devicechild.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ID3D10DeviceChild, ID3D10DeviceChild interface [Direct3D 10], ID3D10DeviceChild interface [Direct3D 10],described, d3d10/ID3D10DeviceChild, direct3d10.id3d10devicechild, e38df520-7753-67fb-6fb9-7bd65b783c01
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10DeviceChild
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DeviceChild interface


## -description


A device-child interface accesses data used by a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10DeviceChild</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10DeviceChild</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10DeviceChild</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8c7fa40-470b-4348-be81-f8702f103def">GetDevice</a>
</td>
<td align="left" width="63%">
Get a pointer to the device that created this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd300d75-3b3e-4ac4-8316-24413e87aa99">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get application-defined data from a device child.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eea3492-1f4f-49ea-88c8-064583ec6910">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set application-defined data to a device child and associate that data with an application-defined guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/774cc86e-5162-418e-9c04-63a4c6f21b63">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface with this device child and associate that interface with an application-defined guid.

</td>
</tr>
</table> 


## -remarks



There are several types of device child interfaces, all of which inherit this interface. They include shaders, state objects, and input layouts.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

