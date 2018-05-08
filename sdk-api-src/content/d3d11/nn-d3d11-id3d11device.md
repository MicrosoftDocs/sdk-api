---
UID: NN:d3d11.ID3D11Device
title: ID3D11Device
author: windows-driver-content
description: The device interface represents a virtual adapter; it is used to create resources.
old-location: direct3d11\id3d11device.htm
old-project: direct3d11
ms.assetid: 2f2559d9-1cd6-44f6-90e2-ee0f86e39f78
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11Device, ID3D11Device interface [Direct3D 11], ID3D11Device interface [Direct3D 11],described, b37b606f-bf79-e387-57c4-bebf1cf88722, d3d11/ID3D11Device, direct3d11.id3d11device
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device interface


## -description


The device interface represents a virtual adapter; it is used to create resources.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://msdn.microsoft.com/C077BAD4-08D2-4F1F-8313-5066F68F014C">ID3D11Device5</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11Device5</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b09feac6-79c8-4f40-bfa1-028d4490b039">CheckCounter</a>
</td>
<td align="left" width="63%">
Get the type, name, units of measure, and a description of an existing counter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c8824e4-33e8-46c4-bcaf-99a68fa56033">CheckCounterInfo</a>
</td>
<td align="left" width="63%">
Get a counter's information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the features that are supported by the current graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5442fe8-e510-4bda-9df0-377b465cdd5e">CheckFormatSupport</a>
</td>
<td align="left" width="63%">
Get the support of a given format on the installed video device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/346f5dae-3ce2-4c03-ab17-1c46e18efc64">CheckMultisampleQualityLevels</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05b27d72-6ae5-4bab-8906-2d1373ea8d4c">CreateBlendState</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aec93c5-12a1-4b4e-813e-ee1e85adbf14">CreateBuffer</a>
</td>
<td align="left" width="63%">
Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d68e977-bcdc-4aab-9434-29200553a69e">CreateClassLinkage</a>
</td>
<td align="left" width="63%">
Creates class linkage libraries to enable dynamic shader linkage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ee0f4f5-48dc-4d5a-b159-c1b7f72e5367">CreateComputeShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/02c1f98e-fdd6-49b0-b8b2-efbd472ab599">compute shader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/857111cc-f590-4383-994c-a72402f8a4aa">CreateCounter</a>
</td>
<td align="left" width="63%">
Create a counter object for measuring GPU performance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">CreateDeferredContext</a>
</td>
<td align="left" width="63%">

      Creates a deferred context, which can record command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7577604c-922c-408c-8eab-2361ebda17df">CreateDepthStencilState</a>
</td>
<td align="left" width="63%">
Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Create a depth-stencil view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/414525a8-55ad-4d37-a302-5c30909588f1">CreateDomainShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">domain shader</a>
.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9357d7-ac63-4515-9118-24a2d775e697">CreateGeometryShader</a>
</td>
<td align="left" width="63%">
Create a geometry shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69499121-6f35-4cf1-b115-9ffdce26e4b0">CreateGeometryShaderWithStreamOutput</a>
</td>
<td align="left" width="63%">
Creates a geometry shader that can write to streaming output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93ec9f46-69c5-4863-bd74-9c8c92fae586">CreateHullShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull shader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe233b7b-3729-428a-8611-e98ea4c5af35">CreateInputLayout</a>
</td>
<td align="left" width="63%">
Create an input-layout object to describe the input-buffer data for the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f013a648-fd11-417b-8f87-36a4be901715">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Create a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5af4e63b-ba85-4c73-82e3-b09579d7ce78">CreatePredicate</a>
</td>
<td align="left" width="63%">
Creates a predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad09a309-862f-462d-8268-62e44397c298">CreateQuery</a>
</td>
<td align="left" width="63%">
This interface encapsulates methods for querying information from the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b49a8dbb-2280-4d5d-ae65-58cde2e9ed10">CreateRasterizerState</a>
</td>
<td align="left" width="63%">
Create a rasterizer state object that tells the rasterizer stage how to behave.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66cf7189-2882-43a4-8732-657402c983db">CreateSamplerState</a>
</td>
<td align="left" width="63%">
Create a sampler-state object that encapsulates sampling information for a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Create a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34cdf984-8b2e-4ed3-a77b-b373752539f6">CreateTexture1D</a>
</td>
<td align="left" width="63%">
Creates an array of <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">1D textures</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">CreateTexture2D</a>
</td>
<td align="left" width="63%">
Create an array of <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">2D textures</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92b31baf-2d64-47fe-bd0d-550f2a65ed9a">CreateTexture3D</a>
</td>
<td align="left" width="63%">
Create a single <a href="https://msdn.microsoft.com/d745093e-2d51-4d45-a88a-caa0ca58b2ba">3D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85b85114-4e3f-407e-879c-ef4c120cb3c1">CreateUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Creates a view for accessing an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06e5105a-ff7e-430a-ab9a-2aefb161894c">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Create a vertex-shader object from a compiled shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/124e1a50-8fae-4af5-8a9f-a56f000ccbe7">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Get the flags used during the call to create the device with <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e09c954-5c61-49fd-b25a-87dc0051a84d">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Get the reason why the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5deddde-4355-4a34-b40a-50006029d590">GetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/746d7cdf-b054-4bfa-a116-5b884fc9bc96">GetFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the feature level of the hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0349f0b8-7696-4d72-bed4-d39b9ac90f6c">GetImmediateContext</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aeb004e-4507-4bf4-bd79-2747feaf5e4d">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get application-defined data from a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc054547-e098-457e-8c8a-a41496234a63">OpenSharedResource</a>
</td>
<td align="left" width="63%">
Give a device access to a shared resource created on a different device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a442a5dc-7931-4464-a6e7-76441e61da5b">SetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a8add57-b209-4096-9132-f3258469bdbd">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set data to a device and associate that data with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65b4461d-bfbb-4de1-84f8-6294fde12980">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.

</td>
</tr>
</table> 


## -remarks




            A device is created using <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

