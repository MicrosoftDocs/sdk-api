---
UID: NN:d3d11.ID3D11Device
title: ID3D11Device
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources.
old-location: direct3d11\id3d11device.htm
tech.root: direct3d11
ms.assetid: 2f2559d9-1cd6-44f6-90e2-ee0f86e39f78
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11Device, ID3D11Device interface [Direct3D 11], ID3D11Device interface [Direct3D 11],described, b37b606f-bf79-e387-57c4-bebf1cf88722, d3d11/ID3D11Device, direct3d11.id3d11device
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device interface


## -description


The device interface represents a virtual adapter; it is used to create resources.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://msdn.microsoft.com/en-us/library/Mt492478(v=VS.85).aspx">ID3D11Device5</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11Device5</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11Device</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476495(v=VS.85).aspx">CheckCounter</a>
</td>
<td align="left" width="63%">
Get the type, name, units of measure, and a description of an existing counter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476496(v=VS.85).aspx">CheckCounterInfo</a>
</td>
<td align="left" width="63%">
Get a counter's information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476497(v=VS.85).aspx">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the features that are supported by the current graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476498(v=VS.85).aspx">CheckFormatSupport</a>
</td>
<td align="left" width="63%">
Get the support of a given format on the installed video device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476499(v=VS.85).aspx">CheckMultisampleQualityLevels</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476500(v=VS.85).aspx">CreateBlendState</a>
</td>
<td align="left" width="63%">
Create a blend-state object that encapsules blend state for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476501(v=VS.85).aspx">CreateBuffer</a>
</td>
<td align="left" width="63%">
Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476502(v=VS.85).aspx">CreateClassLinkage</a>
</td>
<td align="left" width="63%">
Creates class linkage libraries to enable dynamic shader linkage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476503(v=VS.85).aspx">CreateComputeShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/en-us/library/Ff476331(v=VS.85).aspx">compute shader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476504(v=VS.85).aspx">CreateCounter</a>
</td>
<td align="left" width="63%">
Create a counter object for measuring GPU performance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476505(v=VS.85).aspx">CreateDeferredContext</a>
</td>
<td align="left" width="63%">
Creates a deferred context, which can record command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476506(v=VS.85).aspx">CreateDepthStencilState</a>
</td>
<td align="left" width="63%">
Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476507(v=VS.85).aspx">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Create a depth-stencil view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476508(v=VS.85).aspx">CreateDomainShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">domain shader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476509(v=VS.85).aspx">CreateGeometryShader</a>
</td>
<td align="left" width="63%">
Create a geometry shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476510(v=VS.85).aspx">CreateGeometryShaderWithStreamOutput</a>
</td>
<td align="left" width="63%">
Creates a geometry shader that can write to streaming output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476511(v=VS.85).aspx">CreateHullShader</a>
</td>
<td align="left" width="63%">
Create a <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull shader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476512(v=VS.85).aspx">CreateInputLayout</a>
</td>
<td align="left" width="63%">
Create an input-layout object to describe the input-buffer data for the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476513(v=VS.85).aspx">CreatePixelShader</a>
</td>
<td align="left" width="63%">
Create a pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476514(v=VS.85).aspx">CreatePredicate</a>
</td>
<td align="left" width="63%">
Creates a predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476515(v=VS.85).aspx">CreateQuery</a>
</td>
<td align="left" width="63%">
This interface encapsulates methods for querying information from the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476516(v=VS.85).aspx">CreateRasterizerState</a>
</td>
<td align="left" width="63%">
Create a rasterizer state object that tells the rasterizer stage how to behave.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476517(v=VS.85).aspx">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476518(v=VS.85).aspx">CreateSamplerState</a>
</td>
<td align="left" width="63%">
Create a sampler-state object that encapsulates sampling information for a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476519(v=VS.85).aspx">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Create a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476520(v=VS.85).aspx">CreateTexture1D</a>
</td>
<td align="left" width="63%">
Creates an array of <a href="https://msdn.microsoft.com/en-us/library/Ff476906(v=VS.85).aspx">1D textures</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476521(v=VS.85).aspx">CreateTexture2D</a>
</td>
<td align="left" width="63%">
Create an array of <a href="https://msdn.microsoft.com/en-us/library/Ff476906(v=VS.85).aspx">2D textures</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476522(v=VS.85).aspx">CreateTexture3D</a>
</td>
<td align="left" width="63%">
Create a single <a href="https://msdn.microsoft.com/en-us/library/Ff476906(v=VS.85).aspx">3D texture</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476523(v=VS.85).aspx">CreateUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Creates a view for accessing an <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">unordered access</a> resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476524(v=VS.85).aspx">CreateVertexShader</a>
</td>
<td align="left" width="63%">
Create a vertex-shader object from a compiled shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476525(v=VS.85).aspx">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Get the flags used during the call to create the device with <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476526(v=VS.85).aspx">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Get the reason why the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476527(v=VS.85).aspx">GetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476528(v=VS.85).aspx">GetFeatureLevel</a>
</td>
<td align="left" width="63%">
Gets the feature level of the hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476529(v=VS.85).aspx">GetImmediateContext</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476530(v=VS.85).aspx">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get application-defined data from a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476531(v=VS.85).aspx">OpenSharedResource</a>
</td>
<td align="left" width="63%">
Give a device access to a shared resource created on a different device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476532(v=VS.85).aspx">SetExceptionMode</a>
</td>
<td align="left" width="63%">
Get the exception-mode flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476533(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Set data to a device and associate that data with a guid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476534(v=VS.85).aspx">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.

</td>
</tr>
</table> 


## -remarks



A device is created using <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

