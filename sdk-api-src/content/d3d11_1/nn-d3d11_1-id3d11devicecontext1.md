---
UID: NN:d3d11_1.ID3D11DeviceContext1
title: ID3D11DeviceContext1
author: windows-sdk-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext1 adds new methods to those in ID3D11DeviceContext.
old-location: direct3d11\id3d11devicecontext1.htm
tech.root: direct3d11
ms.assetid: DD2A556D-AEF0-407E-A497-CF17ACDEB1A7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11DeviceContext1, ID3D11DeviceContext1 interface [Direct3D 11], ID3D11DeviceContext1 interface [Direct3D 11],described, d3d11_1/ID3D11DeviceContext1, direct3d11.id3d11devicecontext1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_1.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext1 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext1</b> adds new methods to those in <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>. <b>ID3D11DeviceContext1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404601(v=VS.85).aspx">ClearView</a>
</td>
<td align="left" width="63%">
Sets all the elements in a resource view to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404604(v=VS.85).aspx">CopySubresourceRegion1</a>
</td>
<td align="left" width="63%">
Copies a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404607(v=VS.85).aspx">CSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the compute-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404610(v=VS.85).aspx">CSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the compute-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404613(v=VS.85).aspx">DiscardResource</a>
</td>
<td align="left" width="63%">
Discards a resource from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404616(v=VS.85).aspx">DiscardView</a>
</td>
<td align="left" width="63%">
Discards a resource view from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/JJ247573(v=VS.85).aspx">DiscardView1</a>
</td>
<td align="left" width="63%">
Discards the specified elements in a resource view from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404630(v=VS.85).aspx">DSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the domain-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404632(v=VS.85).aspx">DSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the domain-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404635(v=VS.85).aspx">GSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the geometry shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404638(v=VS.85).aspx">GSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the geometry shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404641(v=VS.85).aspx">HSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a> uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404642(v=VS.85).aspx">HSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a> of the pipeline uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404645(v=VS.85).aspx">PSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the pixel shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404649(v=VS.85).aspx">PSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the pixel shader pipeline stage uses, and enables the shader to access other parts of the buffer.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446787(v=VS.85).aspx">SwapDeviceContextState</a>
</td>
<td align="left" width="63%">
Activates the given context state object and changes the current device behavior to Direct3D 11, Direct3D 10.1, or Direct3D 10.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446790(v=VS.85).aspx">UpdateSubresource1</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a subresource created in non-mappable memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446793(v=VS.85).aspx">VSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the vertex shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446795(v=VS.85).aspx">VSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the vertex shader pipeline stage uses.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

