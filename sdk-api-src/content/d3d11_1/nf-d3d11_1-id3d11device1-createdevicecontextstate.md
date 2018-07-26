---
UID: NF:d3d11_1.ID3D11Device1.CreateDeviceContextState
title: ID3D11Device1::CreateDeviceContextState
author: windows-sdk-content
description: Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.
old-location: direct3d11\id3d11device1_createdevicecontextstate.htm
old-project: direct3d11
ms.assetid: 8887C3F1-3EA3-4948-A019-E3CB3F3D46C6
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateDeviceContextState, CreateDeviceContextState method [Direct3D 11], CreateDeviceContextState method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateDeviceContextState method, ID3D11Device1.CreateDeviceContextState, ID3D11Device1::CreateDeviceContextState, d3d11_1/ID3D11Device1::CreateDeviceContextState, direct3d11.id3d11device1_createdevicecontextstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device1.CreateDeviceContextState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device1::CreateDeviceContextState


## -description


Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.
      


## -parameters




### -param Flags

A combination of 
              <a href="https://msdn.microsoft.com/45F1C268-AA8A-44D5-BE9E-0C185738EB69">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</a> 
              values that are combined by using a bitwise <b>OR</b> operation. 
              The resulting value specifies how to create the context state object. 
              The 
              <a href="d3d11_1_create_device_context_state_flag.htm">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</a>flag is currently the only defined flag. 
              If the original device was created with 
              <a href="d3d11_create_device_flag.htm">D3D11_CREATE_DEVICE_SINGLETHREADED</a>, 
              you must create all context state objects from that device with the 
              <b>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</b>flag.
            



If you set the single-threaded flag for both the context state object and the device, you guarantee that you will call the whole set of context methods and device methods only from one thread. 
            You therefore do not need to use critical sections to synchronize access to the device context, and the runtime can avoid working with those processor-intensive critical sections.


### -param pFeatureLevels [in]

A pointer to an array of <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a> values. The array can contain elements from the following list and determines the order of feature levels for which creation is attempted.
              Unlike <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>, you can't set <i>pFeatureLevels</i> to <b>NULL</b> because  there is no default feature level array.
            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>{
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1,
};
          </pre>
</td>
</tr>
</table></span></div>

### -param FeatureLevels

The number of elements in <i>pFeatureLevels</i>. Unlike <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>, you must set <i>FeatureLevels</i> to greater than 0 because you can't set <i>pFeatureLevels</i> to <b>NULL</b>.
          


### -param SDKVersion

The SDK version. You must set this parameter to <b>D3D11_SDK_VERSION</b>.
          


### -param EmulatedInterface

The globally unique identifier (GUID) for the emulated interface. This value specifies the behavior of the device when the context state object is active. Valid values are  obtained by using the <b>__uuidof</b> operator on the <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>, <a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1</a>, <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>, and <a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a> interfaces. See Remarks.
          


### -param pChosenFeatureLevel [out, optional]

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a> value from the <i>pFeatureLevels</i> array. This is the first array value with which <b>CreateDeviceContextState</b> succeeded in creating the context state object. If the call to <b>CreateDeviceContextState</b> fails, the variable pointed to by <i>pChosenFeatureLevel</i> is set to zero.
          


### -param ppContextState [out, optional]

The address of a pointer to an <a href="https://msdn.microsoft.com/A8B9CADC-A9C7-4691-BB5C-3C12FF638C98">ID3DDeviceContextState</a> object that represents the state of a Direct3D device.
          


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



The  <b>REFIID</b> value of the emulated interface is a GUID obtained by use of the <b>__uuidof</b> operator. For example, <code>__uuidof(ID3D11Device)</code> gets the GUID of the interface to a Microsoft Direct3D 11 device.
        

Call the <a href="https://msdn.microsoft.com/4E267E86-602F-459C-A6F9-4660EC8FA752">ID3D11DeviceContext1::SwapDeviceContextState</a> method to activate the context state object. When the context state object is active, the device behaviors that are associated with both the context state object's feature level and its compatible interface are activated on the Direct3D device until the next call to <b>SwapDeviceContextState</b>.
        

When a context state object is active, the runtime disables certain methods on the device and context interfaces. For example, a context state object that is created with <code>__uuidof(ID3D11Device)</code> will cause the runtime to turn off most of the Microsoft Direct3D 10 device interfaces, and a context state object that is created with <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> will cause the runtime to turn off most of the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> methods.
          This behavior ensures that a user of either emulated interface cannot set device state that the other emulated interface is unable to express. This restriction helps guarantee that the <a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1</a> emulated interface accurately reflects the full state of the pipeline and that the emulated interface will not operate contrary to its original interface definition.
        

For example, suppose the tessellation stage is made active through the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface
          when you create the device through <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a> or <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>,  instead of through the Direct3D 10 equivalents. Because  the Direct3D 11 context is active, a Direct3D 10 interface is inactive when you first retrieve it via <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>. This means that you cannot  immediately pass a Direct3D 10 interface that you retrieved from a Direct3D 11 device to a function. You must first call <a href="https://msdn.microsoft.com/4E267E86-602F-459C-A6F9-4660EC8FA752">SwapDeviceContextState</a> to activate a Direct3D 10-compatible context state object.
        

The following table shows the methods that are active and inactive for each emulated interface.<table>
<tr>
<th> Emulated interface </th>
<th>Active device or immediate context  interfaces </th>
<th>Inactive device or immediate context  interfaces</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> or
                


<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>


</td>
<td>

<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>



<a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> +
                


<a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a> +
                


<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>



<a href="https://msdn.microsoft.com/ff4890fe-25a3-4515-b20d-45f68637e7b3">ID3D10Multithread</a>


</td>
<td>
<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>
</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1</a> or
                


<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>


</td>
<td>

<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>



<a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1</a>



<a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> +
                


<a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>



<a href="https://msdn.microsoft.com/ff4890fe-25a3-4515-b20d-45f68637e7b3">ID3D10Multithread</a>


</td>
<td>

<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>



<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> (As published by the immediate context. The Direct3D 10 or Microsoft Direct3D 10.1 emulated interface has no effect on deferred contexts.)
                

</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime disables when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/1e2269cf-edef-466e-be59-95dc644c7a0c">ClearDepthStencilView</a>


</td>
<td>

<a href="https://msdn.microsoft.com/ac596c4d-dc54-4433-8625-defa8a04bba0">ClearDepthStencilView</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/bbc6d3fb-b64f-47b0-9feb-a248dce0bf4b">ClearRenderTargetView</a>


</td>
<td>

<a href="https://msdn.microsoft.com/c1a630a3-3ffe-4d6a-a8e2-7a228167adb2">ClearRenderTargetView</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ClearState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/9fb42265-26fc-44c1-aa43-cb87ac475718">ClearState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/73e70330-63cb-4ba6-b6e5-fc9707fb9f31">ClearUnorderedAccessViewUint</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c93d8638-c624-402a-8e14-c85aa7b69930">ClearUnorderedAccessViewFloat</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/54c1c08a-792c-463d-8237-9f7947d15396">CopyResource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">CopyResource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d4f8576f-8d23-4b45-a5ea-099c71e8567e">CopyStructureCount</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">CopySubresourceRegion</a>


</td>
<td>

<a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">CopySubresourceRegion</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9ffd4fb5-9e7f-4a1b-b7ad-3c7384406385">CSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/97f5be84-3562-4b5a-9c7a-2ac3f18a184b">CSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ddd09ca8-ab1f-4d1d-a182-44e48bac93c5">CSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/872dac3b-8461-4150-b51f-ce02f7356754">CSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ae572062-0034-48c2-a3ce-abe40b50248b">CSGetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/40970d1d-bad3-48e0-8f0e-6d45fe602594">CSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8b7f5c6d-0d9d-4b8b-a812-1e2b3b7386e9">CSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/97be7622-609f-4576-911a-93aa7f1b6b8c">CSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/04babe17-b053-49f4-90bc-8080f521079e">CSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/384a15c0-a035-4f83-a927-e2f763e5fb44">CSSetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">Dispatch</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/bb8840f5-ae4b-42d6-b51d-6844d0b18074">DispatchIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/4a5b000d-769b-4e4c-9c9c-d8fced703812">CreateBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9c63067b-c7ac-412c-ad49-c35d4fba1d68">Draw</a>


</td>
<td>

<a href="https://msdn.microsoft.com/01847bc8-3a58-4296-9e67-2fecd3832e48">Draw</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/34688e87-514f-4f85-b56b-e0245400a5ac">DrawAuto</a>


</td>
<td>

<a href="https://msdn.microsoft.com/22261780-2768-4ea2-9e92-57ae5560e8fe">DrawAuto</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/461a64ec-f3e6-4f6a-8bc4-a349d19501a8">DrawIndexed</a>


</td>
<td>

<a href="https://msdn.microsoft.com/10c4a734-6425-4bd1-ac8e-85e3255e732a">DrawIndexed</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c7a4821a-324c-47e4-b89f-603d2afcfb51">DrawIndexedInstanced</a>


</td>
<td>

<a href="https://msdn.microsoft.com/00713e51-0bc6-4141-a10a-ab998666cdb4">DrawIndexedInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c6969210-b452-4a49-a3d7-d849b1d2ebb5">DrawIndexedInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/3cb608e7-d64d-42cc-9b34-5f6c30af2ada">DrawInstanced</a>


</td>
<td>

<a href="https://msdn.microsoft.com/de2cc0de-7bf3-4b03-a3de-65f841bfc228">DrawInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f40c662d-7cdc-4592-b8d5-72aad0b4dd53">DrawInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/070b3c40-ddb2-4c13-b0a0-1451e00e0ae1">DSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9cb6fee7-0dda-472c-b2e0-36d52e7f12b7">DSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b04a9640-e28e-419e-9a8c-02685e7a0883">DSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/6308e37c-a30f-4927-946b-33d882f9cce8">DSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ae2b8269-59b0-44e9-8173-89baf20436f1">DSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/15cc8f81-2d57-4148-821c-0136c0ce3f82">DSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5ee4a072-3b4a-44e6-ae70-19e0888905a2">DSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/633aedf7-f5cc-4873-940a-1b6e15927ec6">DSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/54e74f7d-b8a4-458d-bb39-3d8a824f06ef">ExecuteCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/31e9d8b6-4173-4999-8772-75134d60d269">FinishCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>


</td>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/43012c58-3b1a-4956-993f-4ff3f5ec7fce">GenerateMips</a>


</td>
<td>

<a href="https://msdn.microsoft.com/bc3491b6-99fb-4560-bce1-dd7758626cf9">GenerateMips</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9a283895-51c4-4de5-bdeb-994f3085bd79">GetPredication</a>


</td>
<td>

<a href="https://msdn.microsoft.com/20cafa97-0677-4660-a889-01e99668b04f">GetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/335f9394-064a-4a2c-b581-323a4a4fde70">GetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/d9f1d623-d0ff-4613-bead-00e2439c8ace">GetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/1a28c673-1e37-4801-bb9c-ba0cf28335d1">GSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/ce3c33fe-4f6c-4395-9eb7-a4fb9b21984d">GSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7f3d4eb4-30e6-42bf-98e2-08a9abcb3e94">GSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/a8d73dab-f81b-4858-9e30-a25c969d0290">GSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5d5b935f-7eef-48ee-a2ed-82dd6c59aa19">GSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/0d848f51-a06c-4757-b79c-6c7a31b06b6b">GSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2b81a09d-678d-42f8-8935-6d167509fcbb">GSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/ca76febd-72ca-4a07-b5cc-8490a8792dab">GSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2af7ab0c-4a21-474c-9a17-ed90f89285fd">GSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/b736c9db-e0c0-4c38-a58a-7b3c247e374d">GSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8e624e36-692e-4710-a267-05b73a089cd9">GSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/881cea8b-eb37-4614-b4dc-81a3e8c929d3">GSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/6c42d028-b832-470c-ab15-1cf46a3f8414">GSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/cd591f9d-dd17-48e3-b952-9f38c7572b93">GSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">GSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">GSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/82987afa-fcb4-4d87-ab53-916a9dac3609">HSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/68200f28-85af-4275-8e9e-7f093fd94a0c">HSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2ac2d88f-8c66-490e-add8-95ecaadf0147">HSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/21956575-5f4b-48ca-944b-5cab57d02c7f">HSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8e3007ac-de5e-45ee-bb58-644dc857c279">HSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f573f65b-abd4-4ddd-9471-032c2c5552d7">HSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/e540f88f-fbf8-4135-b1ee-873ec18bc2c8">HSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/cb99cb22-a7e4-4472-b519-12bced9a45b8">HSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/948a5cbd-8413-4aaa-b666-7b9adc4705da">IAGetIndexBuffer</a>


</td>
<td>

<a href="https://msdn.microsoft.com/744cf15e-524b-4287-9482-b590ab30148c">IAGetIndexBuffer</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b3d07e01-405e-4973-956f-85a08b720aaa">IAGetInputLayout</a>


</td>
<td>

<a href="https://msdn.microsoft.com/50b7ff83-2ce2-4805-a20b-a5329d2a955c">IAGetInputLayout</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/99f82993-72c2-47b5-a2fe-16bb1e7bd2e3">IAGetPrimitiveTopology</a>


</td>
<td>

<a href="https://msdn.microsoft.com/1662dd95-df26-4f0c-9f12-07d958bfb3aa">IAGetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/13b1eb06-effa-4483-993a-da47ee0b916f">IAGetVertexBuffers</a>
</td>
<td>

<a href="https://msdn.microsoft.com/7dc43a98-b7f8-4276-802a-147ee8abf437">IAGetVertexBuffers</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c556dda2-0808-4701-90cb-16c67a24add1">IASetIndexBuffer</a>
</td>
<td>

<a href="https://msdn.microsoft.com/2b276345-502e-47fa-9caa-52a82916b577">IASetIndexBuffer</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54562ece-db8d-4e31-bde2-36391792e259">IASetInputLayout</a>
</td>
<td>

<a href="https://msdn.microsoft.com/10270e52-8ba6-45a6-a6f2-80e3f3447806">IASetInputLayout</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a9896b34-b273-4be2-bea4-0fcecdf5bcad">IASetPrimitiveTopology</a>
</td>
<td>

<a href="https://msdn.microsoft.com/c39db604-7d00-4b22-8bbe-9eda6908c3a1">IASetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e9a9a69c-7df7-4784-98f5-9ad63f6cd407">IASetVertexBuffers</a>
</td>
<td>

<a href="https://msdn.microsoft.com/00fcf32c-982f-4636-bf02-b3f95803684a">IASetVertexBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/871429b4-8f4a-43bb-ae55-3b07f8d00f68">OMGetBlendState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/da49b042-c6e1-41e9-8e49-238de090d502">OMGetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d5ea53a8-62c9-46c9-96ed-8c9977d916b2">OMGetDepthStencilState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/18aa270d-5806-4f3d-b2a1-88481cc2560a">OMGetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/27ac656a-0906-43ad-8089-b41639b55ecf">OMGetRenderTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/9157ec59-f916-40cd-80b0-68d9f63c4db9">OMGetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5baaedea-5db4-4a25-adfc-2ac9cf48ad6d">OMGetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/fabcae1d-2ad8-4f4d-8eef-18945e369225">OMSetBlendState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">OMSetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/cd5642c4-8bbe-4b5d-9f04-87de82ee9601">OMSetDepthStencilState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/7cf8e5ca-08f2-4fa3-8657-cbce5d773dcf">OMSetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">OMSetRenderTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">OMSetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/1973d40f-f0d0-497e-be7b-6cf55f8a7da2">OMSetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/798c1d22-cfe2-45f4-b220-40a7a7ab4bf5">PSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/dbf82053-540b-4629-9bc2-be249eed1336">PSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8a86f6c8-4095-48d5-a3aa-a3eef9f4b3e8">PSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/654ba7fe-f807-40b0-8510-7f37c2067dcd">PSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/6ebeb763-b517-468c-bd46-022a426e0b6e">PSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/6499083a-6c0f-42b4-a43b-9c4f9cb82edd">PSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5b8af19e-a675-42f5-85ef-232b0bb7dd6d">PSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/063a391b-3a0b-4f87-ab67-7a0df8e82ccb">PSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/03e5f255-3a5d-4c77-ad3b-5a188c9eb35b">PSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/3d8de009-8a56-458c-bb62-de36ae094717">PSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b344c0fb-056d-452d-9d30-a8f97e7d226a">PSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/2684b37d-8f10-4c32-8c52-fc2e5bf2122c">PSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2ee5c946-10bd-40b0-90b2-015aff2377aa">PSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/8e7cf7fb-e2c0-4524-a909-5592decd9a66">PSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">PSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">PSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7b4d6180-e3bf-475a-9865-592cda6e9f4a">ResolveSubresource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/cf2e9849-dbd8-4047-8e34-88fca5409bc9">ResolveSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/83676c65-e5d8-44c9-bc0d-ebe9850cb382">RSGetScissorRects</a>


</td>
<td>

<a href="https://msdn.microsoft.com/64a1e3eb-b7ff-4665-8b9a-b33d76be0953">RSGetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/bd1ade36-e57c-4776-ab59-ba8b59276369">RSGetState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/a088c319-9f85-4170-b29d-e786d53e0c4d">RSGetState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9932182f-8e62-41fe-9004-7fb0b591630f">RSGetViewports</a>


</td>
<td>

<a href="https://msdn.microsoft.com/878637b8-ecc6-4580-82d4-f4b990bba9c8">RSGetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/80bee89d-1743-475c-a284-8137cfacdac2">RSSetScissorRects</a>


</td>
<td>

<a href="https://msdn.microsoft.com/38b1d970-ecbd-45cc-a4c5-76f671247e56">RSSetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/aa76cd3f-5d08-48e7-bd38-ff4d7119eae3">RSSetState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/6b873af4-9724-4a36-bfdd-ea47c667124f">RSSetState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7326e9a8-edfa-4e5a-a29e-fe7c54a055f5">RSSetViewports</a>


</td>
<td>

<a href="https://msdn.microsoft.com/d622c531-8cd5-46f6-82dd-27a202c2b58f">RSSetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ceac248a-31c9-4e14-892f-f047e288daae">SetPredication</a>


</td>
<td>

<a href="https://msdn.microsoft.com/175c4905-834a-4f18-bbf6-3bbe20e06d4d">SetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c718bc0b-fb3b-49fd-91f1-098edc0c115d">SetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/af4eda3a-3348-41f5-a474-28af082dfed9">SetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/878402ed-0c89-42db-8210-d9a90b347226">SOGetTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/83753497-3f00-4c5d-9b75-13269b06bdc2">SOGetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/fba6e33e-7d35-4f26-b841-38610164d276">SOSetTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/fd4a71a1-2180-421f-8c9b-735c33f6de75">SOSetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">UpdateSubresource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/eeab4057-4827-4c4b-ae8d-1cbf1f1c9e44">UpdateSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d31bff37-4109-40af-bc75-7e73582d6fa1">VSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/dfb614c5-2e83-45e7-80a1-24d66d170b3d">VSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/0b8cbdfe-58e1-46f0-86c1-22da8178d296">VSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/fb35c064-b308-40a3-ae77-7b4e8819fffa">VSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/03347303-bab2-46aa-81e8-7df75911ff21">VSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/d4922ef4-ff5a-4664-ac37-68facb7c7314">VSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9b7974ea-3194-412d-8040-2d93280f77ac">VSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/8f2247e0-0d30-4ea0-a470-0ec38f33a0c8">VSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c6f9674b-89fe-4e1e-b814-6ddd98a9cb98">VSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/cf5a2172-a4ca-4e76-ae79-d5fbf5bcb155">VSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/bfbf557c-f355-4d4d-beb0-f36e1c6f32ed">VSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/4310c4dc-7fb4-4b69-9bc5-e89761d2e34c">VSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d6207779-7477-4e74-beb8-065949abce06">VSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/9ebc673d-d3e0-4678-8c6e-b11fb75e1ed1">VSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">VSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">VSSetShaderResources</a>


</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime does not disable when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">Begin</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">End</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/490126d3-7298-4f88-9703-3dc2dd30c0a8">GetCreationFlags</a>


</td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/ba0be621-d063-425f-a87f-ded0135c6434">GetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/063fbcaf-2216-4090-a4cb-79091ed9b87a">GetContextFlags</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">Map</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/67797b77-c0a5-47b4-ba54-4282b6aa5b13">Unmap</a>


</td>
<td></td>
</tr>
</table>
 



The following table shows the <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a> interface methods that the runtime does not disable because they are not immediate context methods.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/a36399af-088f-47b2-a580-d871f9e92038">CheckCounter</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/dfa4cc61-2c1d-45a7-839c-f7df64d488ac">CheckCounterInfo</a>


</td>
</tr>
<tr>
<td>
Create*, like <a href="https://msdn.microsoft.com/d8313b54-6aa8-4a41-9dbd-9c175bf6a1d2">CreateQuery</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/e2c2085b-f0d8-4227-81dd-c37907920564">GetDeviceRemovedReason</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/c343ba41-4fec-4598-8eac-30674ab77a49">GetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/581117dc-dd3a-47ac-a080-f23e72a82a6f">OpenSharedResource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/bd15256d-4dc8-43d5-87de-2d35956dc0bd">SetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/1fc318f0-feeb-4aac-91e8-ee9e4d785f40">SetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/71d529a1-acaf-49a9-a4c7-6896979c8909">SetPrivateDataInterface</a>


</td>
</tr>
</table>
 



<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>
 

 

