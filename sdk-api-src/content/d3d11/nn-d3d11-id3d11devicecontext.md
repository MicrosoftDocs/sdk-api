---
UID: NN:d3d11.ID3D11DeviceContext
title: ID3D11DeviceContext
author: windows-sdk-content
description: The ID3D11DeviceContext interface represents a device context which generates rendering commands.
old-location: direct3d11\id3d11devicecontext.htm
tech.root: direct3d11
ms.assetid: afb32c09-77f2-4c33-bd93-8dce92a2e45e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 12a95af1-0ccb-3aa6-2a85-b8822bf74961, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], ID3D11DeviceContext interface [Direct3D 11],described, d3d11/ID3D11DeviceContext, direct3d11.id3d11devicecontext
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
 - ID3D11DeviceContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext interface


## -description


The <b>ID3D11DeviceContext</b> interface represents a device context which generates rendering commands.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://msdn.microsoft.com/en-us/library/Mt492481(v=VS.85).aspx">ID3D11DeviceContext4</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11DeviceContext4</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11DeviceContext</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476386(v=VS.85).aspx">Begin</a>
</td>
<td align="left" width="63%">
Mark the beginning of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476387(v=VS.85).aspx">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476388(v=VS.85).aspx">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476389(v=VS.85).aspx">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476390(v=VS.85).aspx">ClearUnorderedAccessViewFloat</a>
</td>
<td align="left" width="63%">
Clears an <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">unordered access</a> resource with a float value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476391(v=VS.85).aspx">ClearUnorderedAccessViewUint</a>
</td>
<td align="left" width="63%">
Clears an <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">unordered access</a> resource with bit-precise values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476392(v=VS.85).aspx">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476393(v=VS.85).aspx">CopyStructureCount</a>
</td>
<td align="left" width="63%">
Copies data from a buffer holding variable length data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476394(v=VS.85).aspx">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476395(v=VS.85).aspx">CSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476396(v=VS.85).aspx">CSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476397(v=VS.85).aspx">CSGetShader</a>
</td>
<td align="left" width="63%">
Get the compute shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476398(v=VS.85).aspx">CSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the compute-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476399(v=VS.85).aspx">CSGetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Gets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476400(v=VS.85).aspx">CSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476401(v=VS.85).aspx">CSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476402(v=VS.85).aspx">CSSetShader</a>
</td>
<td align="left" width="63%">
Set a compute shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476403(v=VS.85).aspx">CSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476404(v=VS.85).aspx">CSSetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Sets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476405(v=VS.85).aspx">Dispatch</a>
</td>
<td align="left" width="63%">
Execute a command list from a thread group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476406(v=VS.85).aspx">DispatchIndirect</a>
</td>
<td align="left" width="63%">
Execute a command list over one or more thread groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476407(v=VS.85).aspx">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476408(v=VS.85).aspx">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476409(v=VS.85).aspx">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476410(v=VS.85).aspx">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476411(v=VS.85).aspx">DrawIndexedInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476412(v=VS.85).aspx">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476413(v=VS.85).aspx">DrawInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476414(v=VS.85).aspx">DSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476415(v=VS.85).aspx">DSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476416(v=VS.85).aspx">DSGetShader</a>
</td>
<td align="left" width="63%">
Get the domain shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476417(v=VS.85).aspx">DSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the domain-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476418(v=VS.85).aspx">DSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476419(v=VS.85).aspx">DSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476420(v=VS.85).aspx">DSSetShader</a>
</td>
<td align="left" width="63%">
Set a domain shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476421(v=VS.85).aspx">DSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476422(v=VS.85).aspx">End</a>
</td>
<td align="left" width="63%">
Mark the end of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476423(v=VS.85).aspx">ExecuteCommandList</a>
</td>
<td align="left" width="63%">
Queues commands from a command list onto a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476424(v=VS.85).aspx">FinishCommandList</a>
</td>
<td align="left" width="63%">
Create a command list and record graphics commands into it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476425(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Sends queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476426(v=VS.85).aspx">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476427(v=VS.85).aspx">GetContextFlags</a>
</td>
<td align="left" width="63%">
Gets the initialization flags associated with the current deferred context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476428(v=VS.85).aspx">GetData</a>
</td>
<td align="left" width="63%">
Get data from the GPU asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476429(v=VS.85).aspx">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476430(v=VS.85).aspx">GetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Gets the minimum level-of-detail (LOD).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476431(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of <a href="https://msdn.microsoft.com/en-us/library/Ff476880(v=VS.85).aspx">device context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476432(v=VS.85).aspx">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476433(v=VS.85).aspx">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476434(v=VS.85).aspx">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476435(v=VS.85).aspx">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476436(v=VS.85).aspx">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476437(v=VS.85).aspx">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476438(v=VS.85).aspx">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476439(v=VS.85).aspx">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the geometry shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476440(v=VS.85).aspx">HSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476441(v=VS.85).aspx">HSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476442(v=VS.85).aspx">HSGetShader</a>
</td>
<td align="left" width="63%">
Get the hull shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476443(v=VS.85).aspx">HSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the hull-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476445(v=VS.85).aspx">HSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the constant buffers used by the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476446(v=VS.85).aspx">HSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476447(v=VS.85).aspx">HSSetShader</a>
</td>
<td align="left" width="63%">
Set a hull shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476448(v=VS.85).aspx">HSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476449(v=VS.85).aspx">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the index buffer that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476450(v=VS.85).aspx">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476451(v=VS.85).aspx">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476452(v=VS.85).aspx">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the vertex buffers bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476453(v=VS.85).aspx">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an index buffer to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476454(v=VS.85).aspx">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476455(v=VS.85).aspx">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476456(v=VS.85).aspx">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of vertex buffers to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476457(v=VS.85).aspx">Map</a>
</td>
<td align="left" width="63%">
Gets a pointer to the data contained in a <a href="https://msdn.microsoft.com/en-us/library/Ff476901(v=VS.85).aspx">subresource</a>, and denies the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476458(v=VS.85).aspx">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476459(v=VS.85).aspx">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476460(v=VS.85).aspx">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476461(v=VS.85).aspx">OMGetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476462(v=VS.85).aspx">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476463(v=VS.85).aspx">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476464(v=VS.85).aspx">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets atomically and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476465(v=VS.85).aspx">OMSetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Binds resources to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476466(v=VS.85).aspx">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476467(v=VS.85).aspx">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476468(v=VS.85).aspx">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476469(v=VS.85).aspx">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476470(v=VS.85).aspx">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476471(v=VS.85).aspx">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476472(v=VS.85).aspx">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476473(v=VS.85).aspx">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the pixel shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476474(v=VS.85).aspx">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476475(v=VS.85).aspx">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of scissor rectangles bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476476(v=VS.85).aspx">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/en-us/library/Ff476198(v=VS.85).aspx">rasterizer state</a> from the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476477(v=VS.85).aspx">RSGetViewports</a>
</td>
<td align="left" width="63%">
Gets the array of viewports bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476478(v=VS.85).aspx">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of scissor rectangles to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476479(v=VS.85).aspx">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/en-us/library/Ff476198(v=VS.85).aspx">rasterizer state</a> for the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476480(v=VS.85).aspx">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of viewports to the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476481(v=VS.85).aspx">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476482(v=VS.85).aspx">SetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Sets the minimum level-of-detail (LOD) for a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476483(v=VS.85).aspx">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476484(v=VS.85).aspx">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476485(v=VS.85).aspx">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource and reenable the GPU's access to that resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476486(v=VS.85).aspx">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a subresource created in non-mappable memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476487(v=VS.85).aspx">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476488(v=VS.85).aspx">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476489(v=VS.85).aspx">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476490(v=VS.85).aspx">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476491(v=VS.85).aspx">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476492(v=VS.85).aspx">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476493(v=VS.85).aspx">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476494(v=VS.85).aspx">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the vertex-shader stage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

