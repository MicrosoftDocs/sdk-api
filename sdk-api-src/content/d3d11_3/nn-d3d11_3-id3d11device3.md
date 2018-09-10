---
UID: NN:d3d11_3.ID3D11Device3
title: ID3D11Device3
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device3 adds new methods to those in ID3D11Device2.
old-location: direct3d11\id3d11device3.htm
tech.root: direct3d11
ms.assetid: 0AA10851-0077-4075-BD41-72FCD7BC0556
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Device3, ID3D11Device3 interface [Direct3D 11], ID3D11Device3 interface [Direct3D 11],described, d3d11_3/ID3D11Device3, direct3d11.id3d11device3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11Device3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device3 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device3</b> adds new methods to those in <a href="https://msdn.microsoft.com/en-us/library/Dn280493(v=VS.85).aspx">ID3D11Device2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn280493(v=VS.85).aspx">ID3D11Device2</a>. <b>ID3D11Device3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn912871(v=VS.85).aspx">CreateDeferredContext3</a>
</td>
<td align="left" width="63%">
Creates a deferred context, which can record <a href="https://msdn.microsoft.com/en-us/library/Ff476885(v=VS.85).aspx">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899220(v=VS.85).aspx">CreateQuery1</a>
</td>
<td align="left" width="63%">
Creates a query object for querying information from the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899221(v=VS.85).aspx">CreateRasterizerState2</a>
</td>
<td align="left" width="63%">
Creates a rasterizer state object that informs the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899224(v=VS.85).aspx">CreateRenderTargetView1</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899227(v=VS.85).aspx">CreateShaderResourceView1</a>
</td>
<td align="left" width="63%">
Creates a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899229(v=VS.85).aspx">CreateTexture2D1</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/Ff476906(v=VS.85).aspx">2D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899231(v=VS.85).aspx">CreateTexture3D1</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/Ff476906(v=VS.85).aspx">3D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899232(v=VS.85).aspx">CreateUnorderedAccessView1</a>
</td>
<td align="left" width="63%">
Creates a view for accessing an <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">unordered access</a> resource.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn912872(v=VS.85).aspx">GetImmediateContext3</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/en-us/library/Ff476885(v=VS.85).aspx">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn912873(v=VS.85).aspx">ReadFromSubresource</a>
</td>
<td align="left" width="63%">
Copies data from a
          <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DEFAULT</a>texture which was mapped using
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/en-us/library/Ff476457(v=VS.85).aspx">Map</a>while providing a NULL
          <a href="https://msdn.microsoft.com/en-us/library/Ff476182(v=VS.85).aspx">D3D11_MAPPED_SUBRESOURCE</a>parameter.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn912874(v=VS.85).aspx">WriteToSubresource</a>
</td>
<td align="left" width="63%">
Copies data into a
          <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DEFAULT</a>texture which was mapped using
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/en-us/library/Ff476457(v=VS.85).aspx">Map</a>while providing a NULL
          <a href="https://msdn.microsoft.com/en-us/library/Ff476182(v=VS.85).aspx">D3D11_MAPPED_SUBRESOURCE</a>parameter.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn280493(v=VS.85).aspx">ID3D11Device2</a>
 

 

