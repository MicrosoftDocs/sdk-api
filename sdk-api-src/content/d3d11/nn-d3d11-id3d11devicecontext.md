---
UID: NN:d3d11.ID3D11DeviceContext
title: ID3D11DeviceContext (d3d11.h)
description: The ID3D11DeviceContext interface represents a device context which generates rendering commands.
helpviewer_keywords: ["12a95af1-0ccb-3aa6-2a85-b8822bf74961","ID3D11DeviceContext","ID3D11DeviceContext interface [Direct3D 11]","ID3D11DeviceContext interface [Direct3D 11]","described","d3d11/ID3D11DeviceContext","direct3d11.id3d11devicecontext"]
old-location: direct3d11\id3d11devicecontext.htm
tech.root: direct3d11
ms.assetid: afb32c09-77f2-4c33-bd93-8dce92a2e45e
ms.date: 12/05/2018
ms.keywords: 12a95af1-0ccb-3aa6-2a85-b8822bf74961, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], ID3D11DeviceContext interface [Direct3D 11],described, d3d11/ID3D11DeviceContext, direct3d11.id3d11devicecontext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext
 - d3d11/ID3D11DeviceContext
dev_langs:
 - c++
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
---

# ID3D11DeviceContext interface


## -description

The <b>ID3D11DeviceContext</b> interface represents a device context which generates rendering commands.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4">ID3D11DeviceContext4</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11DeviceContext4</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11DeviceContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>
</td>
<td align="left" width="63%">
Mark the beginning of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cleardepthstencilview">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewfloat">ClearUnorderedAccessViewFloat</a>
</td>
<td align="left" width="63%">
Clears an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource with a float value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewuint">ClearUnorderedAccessViewUint</a>
</td>
<td align="left" width="63%">
Clears an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource with bit-precise values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount">CopyStructureCount</a>
</td>
<td align="left" width="63%">
Copies data from a buffer holding variable length data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetconstantbuffers">CSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetsamplers">CSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetshader">CSGetShader</a>
</td>
<td align="left" width="63%">
Get the compute shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetshaderresources">CSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the compute-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetunorderedaccessviews">CSGetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Gets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetconstantbuffers">CSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetsamplers">CSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetshader">CSSetShader</a>
</td>
<td align="left" width="63%">
Set a compute shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetshaderresources">CSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews">CSSetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Sets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">Dispatch</a>
</td>
<td align="left" width="63%">
Execute a command list from a thread group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect">DispatchIndirect</a>
</td>
<td align="left" width="63%">
Execute a command list over one or more thread groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-draw">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstanced">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstancedindirect">DrawIndexedInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstanced">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstancedindirect">DrawInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers">DSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetsamplers">DSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetshader">DSGetShader</a>
</td>
<td align="left" width="63%">
Get the domain shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetshaderresources">DSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the domain-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers">DSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetsamplers">DSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetshader">DSSetShader</a>
</td>
<td align="left" width="63%">
Set a domain shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetshaderresources">DSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">End</a>
</td>
<td align="left" width="63%">
Mark the end of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-executecommandlist">ExecuteCommandList</a>
</td>
<td align="left" width="63%">
Queues commands from a command list onto a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-finishcommandlist">FinishCommandList</a>
</td>
<td align="left" width="63%">
Create a command list and record graphics commands into it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">Flush</a>
</td>
<td align="left" width="63%">
Sends queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getcontextflags">GetContextFlags</a>
</td>
<td align="left" width="63%">
Gets the initialization flags associated with the current deferred context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">GetData</a>
</td>
<td align="left" width="63%">
Get data from the GPU asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getpredication">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getresourceminlod">GetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Gets the minimum level-of-detail (LOD).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-intro">device context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetconstantbuffers">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetsamplers">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetshader">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetshaderresources">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetsamplers">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshader">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshaderresources">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the geometry shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers">HSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetsamplers">HSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetshader">HSGetShader</a>
</td>
<td align="left" width="63%">
Get the hull shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetshaderresources">HSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the hull-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers">HSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the constant buffers used by the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetsamplers">HSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetshader">HSSetShader</a>
</td>
<td align="left" width="63%">
Set a hull shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetshaderresources">HSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetindexbuffer">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the index buffer that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetinputlayout">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetprimitivetopology">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetvertexbuffers">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the vertex buffers bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetindexbuffer">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an index buffer to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetinputlayout">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of vertex buffers to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a>
</td>
<td align="left" width="63%">
Gets a pointer to the data contained in a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-subresources">subresource</a>, and denies the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetblendstate">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetdepthstencilstate">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetrendertargets">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetrendertargetsandunorderedaccessviews">OMGetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets atomically and the depth-stencil buffer to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews">OMSetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Binds resources to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetconstantbuffers">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetsamplers">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetshader">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetshaderresources">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetsamplers">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshaderresources">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the pixel shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetscissorrects">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of scissor rectangles bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetstate">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">rasterizer state</a> from the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetviewports">RSGetViewports</a>
</td>
<td align="left" width="63%">
Gets the array of viewports bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetscissorrects">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of scissor rectangles to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">rasterizer state</a> for the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetviewports">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of viewports to the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setpredication">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setresourceminlod">SetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Sets the minimum level-of-detail (LOD) for a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sogettargets">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sosettargets">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-unmap">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource and reenable the GPU's access to that resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a subresource created in non-mappable memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetconstantbuffers">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetsamplers">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetshader">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetshaderresources">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetsamplers">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshader">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the vertex-shader stage.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>