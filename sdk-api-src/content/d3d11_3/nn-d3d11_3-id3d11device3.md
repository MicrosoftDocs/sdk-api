---
UID: NN:d3d11_3.ID3D11Device3
title: ID3D11Device3
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device3 adds new methods to those in ID3D11Device2.
old-location: direct3d11\id3d11device3.htm
old-project: direct3d11
ms.assetid: 0AA10851-0077-4075-BD41-72FCD7BC0556
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Device3, ID3D11Device3 interface [Direct3D 11], ID3D11Device3 interface [Direct3D 11],described, d3d11_3/ID3D11Device3, direct3d11.id3d11device3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
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
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device3
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device3 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device3</b> adds new methods to those in <a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device3</b> interface inherits from <a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>. <b>ID3D11Device3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/78B52E38-3256-4151-96DA-4C81A2A516CF">CreateDeferredContext3</a>
</td>
<td align="left" width="63%">

          Creates a deferred context, which can record <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D170F97-DA95-48FE-84F6-2BBB3E388BB4">CreateQuery1</a>
</td>
<td align="left" width="63%">
Creates a query object for querying information from the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42BA8F50-7D86-4411-AE05-74F492761DBD">CreateRasterizerState2</a>
</td>
<td align="left" width="63%">
Creates a rasterizer state object that informs the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9B85B007-F8B0-43C1-999E-75E5243B7B5A">CreateRenderTargetView1</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50E072F2-EC3E-4BED-A230-5447ECD1E7D6">CreateShaderResourceView1</a>
</td>
<td align="left" width="63%">
Creates a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50C5789A-2C8E-49CB-9348-639CF8B971EC">CreateTexture2D1</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">2D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EE72AEEF-DBAB-4838-AB91-138EB532BD81">CreateTexture3D1</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">3D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AB64DDED-4C2D-4952-BAA5-3139F973C962">CreateUnorderedAccessView1</a>
</td>
<td align="left" width="63%">

          Creates a view for accessing an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E9E247C3-6326-46AC-A742-F5A4BE701B5B">GetImmediateContext3</a>
</td>
<td align="left" width="63%">

          Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/060B9627-3A95-4DBD-B3E6-3989D8D9C79E">ReadFromSubresource</a>
</td>
<td align="left" width="63%">

          Copies data from a
          <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a>
          texture which was mapped using
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>
          while providing a NULL
          <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a>
          parameter.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DCA4A88D-3DCA-41D5-AE52-061A605A9CBF">WriteToSubresource</a>
</td>
<td align="left" width="63%">

          Copies data into a
          <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a>
          texture which was mapped using
          ID3D11DeviceContext3::<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>
          while providing a NULL
          <a href="https://msdn.microsoft.com/cbbb8689-0a7d-43b9-bde3-29d93cc7f0fe">D3D11_MAPPED_SUBRESOURCE</a>
          parameter.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>
 

 

