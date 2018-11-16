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
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="https://msdn.microsoft.com/9A4B737C-C0A8-4319-A9CA-8172E992774D">ID3D11DeviceContext4</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11DeviceContext4</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11DeviceContext</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>
</td>
<td align="left" width="63%">
Mark the beginning of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e2269cf-edef-466e-be59-95dc644c7a0c">ClearDepthStencilView</a>
</td>
<td align="left" width="63%">
Clears the depth-stencil resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbc6d3fb-b64f-47b0-9feb-a248dce0bf4b">ClearRenderTargetView</a>
</td>
<td align="left" width="63%">
Set all the elements in a render target to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ClearState</a>
</td>
<td align="left" width="63%">
Restore all default settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93d8638-c624-402a-8e14-c85aa7b69930">ClearUnorderedAccessViewFloat</a>
</td>
<td align="left" width="63%">
Clears an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource with a float value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73e70330-63cb-4ba6-b6e5-fc9707fb9f31">ClearUnorderedAccessViewUint</a>
</td>
<td align="left" width="63%">
Clears an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource with bit-precise values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54c1c08a-792c-463d-8237-9f7947d15396">CopyResource</a>
</td>
<td align="left" width="63%">
Copy the entire contents of the source resource to the destination resource using the GPU. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4f8576f-8d23-4b45-a5ea-099c71e8567e">CopyStructureCount</a>
</td>
<td align="left" width="63%">
Copies data from a buffer holding variable length data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">CopySubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ffd4fb5-9e7f-4a1b-b7ad-3c7384406385">CSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97f5be84-3562-4b5a-9c7a-2ac3f18a184b">CSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddd09ca8-ab1f-4d1d-a182-44e48bac93c5">CSGetShader</a>
</td>
<td align="left" width="63%">
Get the compute shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/872dac3b-8461-4150-b51f-ce02f7356754">CSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the compute-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae572062-0034-48c2-a3ce-abe40b50248b">CSGetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Gets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40970d1d-bad3-48e0-8f0e-6d45fe602594">CSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b7f5c6d-0d9d-4b8b-a812-1e2b3b7386e9">CSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97be7622-609f-4576-911a-93aa7f1b6b8c">CSSetShader</a>
</td>
<td align="left" width="63%">
Set a compute shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04babe17-b053-49f4-90bc-8080f521079e">CSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the compute-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/384a15c0-a035-4f83-a927-e2f763e5fb44">CSSetUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Sets an array of views for an unordered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">Dispatch</a>
</td>
<td align="left" width="63%">
Execute a command list from a thread group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb8840f5-ae4b-42d6-b51d-6844d0b18074">DispatchIndirect</a>
</td>
<td align="left" width="63%">
Execute a command list over one or more thread groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c63067b-c7ac-412c-ad49-c35d4fba1d68">Draw</a>
</td>
<td align="left" width="63%">
Draw non-indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34688e87-514f-4f85-b56b-e0245400a5ac">DrawAuto</a>
</td>
<td align="left" width="63%">
Draw geometry of an unknown size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/461a64ec-f3e6-4f6a-8bc4-a349d19501a8">DrawIndexed</a>
</td>
<td align="left" width="63%">
Draw indexed, non-instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a4821a-324c-47e4-b89f-603d2afcfb51">DrawIndexedInstanced</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6969210-b452-4a49-a3d7-d849b1d2ebb5">DrawIndexedInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw indexed, instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cb608e7-d64d-42cc-9b34-5f6c30af2ada">DrawInstanced</a>
</td>
<td align="left" width="63%">
Draw non-indexed, instanced primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f40c662d-7cdc-4592-b8d5-72aad0b4dd53">DrawInstancedIndirect</a>
</td>
<td align="left" width="63%">
Draw instanced, GPU-generated primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/070b3c40-ddb2-4c13-b0a0-1451e00e0ae1">DSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cb6fee7-0dda-472c-b2e0-36d52e7f12b7">DSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b04a9640-e28e-419e-9a8c-02685e7a0883">DSGetShader</a>
</td>
<td align="left" width="63%">
Get the domain shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6308e37c-a30f-4927-946b-33d882f9cce8">DSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the domain-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae2b8269-59b0-44e9-8173-89baf20436f1">DSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15cc8f81-2d57-4148-821c-0136c0ce3f82">DSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee4a072-3b4a-44e6-ae70-19e0888905a2">DSSetShader</a>
</td>
<td align="left" width="63%">
Set a domain shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/633aedf7-f5cc-4873-940a-1b6e15927ec6">DSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the domain-shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">End</a>
</td>
<td align="left" width="63%">
Mark the end of a series of commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54e74f7d-b8a4-458d-bb39-3d8a824f06ef">ExecuteCommandList</a>
</td>
<td align="left" width="63%">
Queues commands from a command list onto a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31e9d8b6-4173-4999-8772-75134d60d269">FinishCommandList</a>
</td>
<td align="left" width="63%">
Create a command list and record graphics commands into it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">Flush</a>
</td>
<td align="left" width="63%">
Sends queued-up commands in the command buffer to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43012c58-3b1a-4956-993f-4ff3f5ec7fce">GenerateMips</a>
</td>
<td align="left" width="63%">
Generates mipmaps for the given shader resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/063fbcaf-2216-4090-a4cb-79091ed9b87a">GetContextFlags</a>
</td>
<td align="left" width="63%">
Gets the initialization flags associated with the current deferred context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">GetData</a>
</td>
<td align="left" width="63%">
Get data from the GPU asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a283895-51c4-4de5-bdeb-994f3085bd79">GetPredication</a>
</td>
<td align="left" width="63%">
Get the rendering predicate state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/335f9394-064a-4a2c-b581-323a4a4fde70">GetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Gets the minimum level-of-detail (LOD).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fefe2cd7-26c1-4165-9c94-8843571f8824">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of <a href="https://msdn.microsoft.com/b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7">device context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a28c673-1e37-4801-bb9c-ba0cf28335d1">GSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f3d4eb4-30e6-42bf-98e2-08a9abcb3e94">GSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d5b935f-7eef-48ee-a2ed-82dd6c59aa19">GSGetShader</a>
</td>
<td align="left" width="63%">
Get the geometry shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b81a09d-678d-42f8-8935-6d167509fcbb">GSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the geometry shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2af7ab0c-4a21-474c-9a17-ed90f89285fd">GSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e624e36-692e-4710-a267-05b73a089cd9">GSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the geometry shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c42d028-b832-470c-ab15-1cf46a3f8414">GSSetShader</a>
</td>
<td align="left" width="63%">
Set a geometry shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">GSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the geometry shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82987afa-fcb4-4d87-ab53-916a9dac3609">HSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68200f28-85af-4275-8e9e-7f093fd94a0c">HSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler state interfaces from the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ac2d88f-8c66-490e-add8-95ecaadf0147">HSGetShader</a>
</td>
<td align="left" width="63%">
Get the hull shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21956575-5f4b-48ca-944b-5cab57d02c7f">HSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the hull-shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e3007ac-de5e-45ee-bb58-644dc857c279">HSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Set the constant buffers used by the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f573f65b-abd4-4ddd-9471-032c2c5552d7">HSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e540f88f-fbf8-4135-b1ee-873ec18bc2c8">HSSetShader</a>
</td>
<td align="left" width="63%">
Set a hull shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb99cb22-a7e4-4472-b519-12bced9a45b8">HSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948a5cbd-8413-4aaa-b666-7b9adc4705da">IAGetIndexBuffer</a>
</td>
<td align="left" width="63%">
Get a pointer to the index buffer that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3d07e01-405e-4973-956f-85a08b720aaa">IAGetInputLayout</a>
</td>
<td align="left" width="63%">
Get a pointer to the input-layout object that is bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99f82993-72c2-47b5-a2fe-16bb1e7bd2e3">IAGetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Get information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13b1eb06-effa-4483-993a-da47ee0b916f">IAGetVertexBuffers</a>
</td>
<td align="left" width="63%">
Get the vertex buffers bound to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c556dda2-0808-4701-90cb-16c67a24add1">IASetIndexBuffer</a>
</td>
<td align="left" width="63%">
Bind an index buffer to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54562ece-db8d-4e31-bde2-36391792e259">IASetInputLayout</a>
</td>
<td align="left" width="63%">
Bind an input-layout object to the input-assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9896b34-b273-4be2-bea4-0fcecdf5bcad">IASetPrimitiveTopology</a>
</td>
<td align="left" width="63%">
Bind information about the primitive type, and data order that describes input data for the input assembler stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9a9a69c-7df7-4784-98f5-9ad63f6cd407">IASetVertexBuffers</a>
</td>
<td align="left" width="63%">
Bind an array of vertex buffers to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>
</td>
<td align="left" width="63%">
Gets a pointer to the data contained in a <a href="https://msdn.microsoft.com/57444cb5-6c8b-4dac-8d6b-ca2b45eafac9">subresource</a>, and denies the GPU access to that subresource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/871429b4-8f4a-43bb-ae55-3b07f8d00f68">OMGetBlendState</a>
</td>
<td align="left" width="63%">
Get the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5ea53a8-62c9-46c9-96ed-8c9977d916b2">OMGetDepthStencilState</a>
</td>
<td align="left" width="63%">
Gets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27ac656a-0906-43ad-8089-b41639b55ecf">OMGetRenderTargets</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5baaedea-5db4-4a25-adfc-2ac9cf48ad6d">OMGetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Get pointers to the resources bound to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fabcae1d-2ad8-4f4d-8eef-18945e369225">OMSetBlendState</a>
</td>
<td align="left" width="63%">
Set the blend state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd5642c4-8bbe-4b5d-9f04-87de82ee9601">OMSetDepthStencilState</a>
</td>
<td align="left" width="63%">
Sets the depth-stencil state of the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">OMSetRenderTargets</a>
</td>
<td align="left" width="63%">
Bind one or more render targets atomically and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1973d40f-f0d0-497e-be7b-6cf55f8a7da2">OMSetRenderTargetsAndUnorderedAccessViews</a>
</td>
<td align="left" width="63%">
Binds resources to the output-merger stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/798c1d22-cfe2-45f4-b220-40a7a7ab4bf5">PSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a86f6c8-4095-48d5-a3aa-a3eef9f4b3e8">PSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ebeb763-b517-468c-bd46-022a426e0b6e">PSGetShader</a>
</td>
<td align="left" width="63%">
Get the pixel shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b8af19e-a675-42f5-85ef-232b0bb7dd6d">PSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the pixel shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03e5f255-3a5d-4c77-ad3b-5a188c9eb35b">PSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b344c0fb-056d-452d-9d30-a8f97e7d226a">PSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the pixel shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ee5c946-10bd-40b0-90b2-015aff2377aa">PSSetShader</a>
</td>
<td align="left" width="63%">
Sets a pixel shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">PSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the pixel shader stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b4d6180-e3bf-475a-9865-592cda6e9f4a">ResolveSubresource</a>
</td>
<td align="left" width="63%">
Copy a multisampled resource into a non-multisampled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83676c65-e5d8-44c9-bc0d-ebe9850cb382">RSGetScissorRects</a>
</td>
<td align="left" width="63%">
Get the array of scissor rectangles bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd1ade36-e57c-4776-ab59-ba8b59276369">RSGetState</a>
</td>
<td align="left" width="63%">
Get the <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">rasterizer state</a> from the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9932182f-8e62-41fe-9004-7fb0b591630f">RSGetViewports</a>
</td>
<td align="left" width="63%">
Gets the array of viewports bound to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80bee89d-1743-475c-a284-8137cfacdac2">RSSetScissorRects</a>
</td>
<td align="left" width="63%">
Bind an array of scissor rectangles to the rasterizer stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa76cd3f-5d08-48e7-bd38-ff4d7119eae3">RSSetState</a>
</td>
<td align="left" width="63%">
Set the <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">rasterizer state</a> for the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7326e9a8-edfa-4e5a-a29e-fe7c54a055f5">RSSetViewports</a>
</td>
<td align="left" width="63%">
Bind an array of viewports to the rasterizer stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ceac248a-31c9-4e14-892f-f047e288daae">SetPredication</a>
</td>
<td align="left" width="63%">
Set a rendering predicate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c718bc0b-fb3b-49fd-91f1-098edc0c115d">SetResourceMinLOD</a>
</td>
<td align="left" width="63%">
Sets the minimum level-of-detail (LOD) for a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/878402ed-0c89-42db-8210-d9a90b347226">SOGetTargets</a>
</td>
<td align="left" width="63%">
Get the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fba6e33e-7d35-4f26-b841-38610164d276">SOSetTargets</a>
</td>
<td align="left" width="63%">
Set the target output buffers for the stream-output stage of the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67797b77-c0a5-47b4-ba54-4282b6aa5b13">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to a resource and reenable the GPU's access to that resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">UpdateSubresource</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a subresource created in non-mappable memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d31bff37-4109-40af-bc75-7e73582d6fa1">VSGetConstantBuffers</a>
</td>
<td align="left" width="63%">
Get the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b8cbdfe-58e1-46f0-86c1-22da8178d296">VSGetSamplers</a>
</td>
<td align="left" width="63%">
Get an array of sampler states from the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03347303-bab2-46aa-81e8-7df75911ff21">VSGetShader</a>
</td>
<td align="left" width="63%">
Get the vertex shader currently set on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b7974ea-3194-412d-8040-2d93280f77ac">VSGetShaderResources</a>
</td>
<td align="left" width="63%">
Get the vertex shader resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6f9674b-89fe-4e1e-b814-6ddd98a9cb98">VSSetConstantBuffers</a>
</td>
<td align="left" width="63%">
Sets the constant buffers used by the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfbf557c-f355-4d4d-beb0-f36e1c6f32ed">VSSetSamplers</a>
</td>
<td align="left" width="63%">
Set an array of sampler states to the vertex shader pipeline stage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6207779-7477-4e74-beb8-065949abce06">VSSetShader</a>
</td>
<td align="left" width="63%">
Set a vertex shader to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">VSSetShaderResources</a>
</td>
<td align="left" width="63%">
Bind an array of shader resources to the vertex-shader stage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

