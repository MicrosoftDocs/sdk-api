---
UID: NF:d3d11_1.ID3D11Device1.CreateDeviceContextState
title: ID3D11Device1::CreateDeviceContextState
author: windows-sdk-content
description: Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.
old-location: direct3d11\id3d11device1_createdevicecontextstate.htm
tech.root: direct3d11
ms.assetid: 8887C3F1-3EA3-4948-A019-E3CB3F3D46C6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateDeviceContextState, CreateDeviceContextState method [Direct3D 11], CreateDeviceContextState method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateDeviceContextState method, ID3D11Device1.CreateDeviceContextState, ID3D11Device1::CreateDeviceContextState, d3d11_1/ID3D11Device1::CreateDeviceContextState, direct3d11.id3d11device1_createdevicecontextstate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11Device1.CreateDeviceContextState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device1::CreateDeviceContextState


## -description


Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.
      


## -parameters




### -param Flags

A combination of 
              <a href="https://msdn.microsoft.com/en-us/library/Hh404432(v=VS.85).aspx">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</a> 
              values that are combined by using a bitwise <b>OR</b> operation. 
              The resulting value specifies how to create the context state object. 
              The 
              <a href="https://msdn.microsoft.com/en-us/library/Hh404432(v=VS.85).aspx">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</a>flag is currently the only defined flag. 
              If the original device was created with 
              <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_SINGLETHREADED</a>, 
              you must create all context state objects from that device with the 
              <b>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</b>flag.
            



If you set the single-threaded flag for both the context state object and the device, you guarantee that you will call the whole set of context methods and device methods only from one thread. 
            You therefore do not need to use critical sections to synchronize access to the device context, and the runtime can avoid working with those processor-intensive critical sections.


### -param pFeatureLevels [in]

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL</a> values. The array can contain elements from the following list and determines the order of feature levels for which creation is attempted.
              Unlike <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a>, you can't set <i>pFeatureLevels</i> to <b>NULL</b> because  there is no default feature level array.
            


```
{
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1,
};
          
```



### -param FeatureLevels

The number of elements in <i>pFeatureLevels</i>. Unlike <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a>, you must set <i>FeatureLevels</i> to greater than 0 because you can't set <i>pFeatureLevels</i> to <b>NULL</b>.
          


### -param SDKVersion

The SDK version. You must set this parameter to <b>D3D11_SDK_VERSION</b>.
          


### -param EmulatedInterface

The globally unique identifier (GUID) for the emulated interface. This value specifies the behavior of the device when the context state object is active. Valid values are  obtained by using the <b>__uuidof</b> operator on the <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1</a>, <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>, and <a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a> interfaces. See Remarks.
          


### -param pChosenFeatureLevel [out, optional]

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL</a> value from the <i>pFeatureLevels</i> array. This is the first array value with which <b>CreateDeviceContextState</b> succeeded in creating the context state object. If the call to <b>CreateDeviceContextState</b> fails, the variable pointed to by <i>pChosenFeatureLevel</i> is set to zero.
          


### -param ppContextState [out, optional]

The address of a pointer to an <a href="https://msdn.microsoft.com/A8B9CADC-A9C7-4691-BB5C-3C12FF638C98">ID3DDeviceContextState</a> object that represents the state of a Direct3D device.
          


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.
          




## -remarks



The  <b>REFIID</b> value of the emulated interface is a GUID obtained by use of the <b>__uuidof</b> operator. For example, <code>__uuidof(ID3D11Device)</code> gets the GUID of the interface to a Microsoft Direct3D 11 device.
        

Call the <a href="https://msdn.microsoft.com/en-us/library/Hh446787(v=VS.85).aspx">ID3D11DeviceContext1::SwapDeviceContextState</a> method to activate the context state object. When the context state object is active, the device behaviors that are associated with both the context state object's feature level and its compatible interface are activated on the Direct3D device until the next call to <b>SwapDeviceContextState</b>.
        

When a context state object is active, the runtime disables certain methods on the device and context interfaces. For example, a context state object that is created with <code>__uuidof(ID3D11Device)</code> will cause the runtime to turn off most of the Microsoft Direct3D 10 device interfaces, and a context state object that is created with <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> will cause the runtime to turn off most of the <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> methods.
          This behavior ensures that a user of either emulated interface cannot set device state that the other emulated interface is unable to express. This restriction helps guarantee that the <a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1</a> emulated interface accurately reflects the full state of the pipeline and that the emulated interface will not operate contrary to its original interface definition.
        

For example, suppose the tessellation stage is made active through the <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> interface
          when you create the device through <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a> or <a href="https://msdn.microsoft.com/en-us/library/Ff476083(v=VS.85).aspx">D3D11CreateDeviceAndSwapChain</a>,  instead of through the Direct3D 10 equivalents. Because  the Direct3D 11 context is active, a Direct3D 10 interface is inactive when you first retrieve it via <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a>. This means that you cannot  immediately pass a Direct3D 10 interface that you retrieved from a Direct3D 11 device to a function. You must first call <a href="https://msdn.microsoft.com/en-us/library/Hh446787(v=VS.85).aspx">SwapDeviceContextState</a> to activate a Direct3D 10-compatible context state object.
        

The following table shows the methods that are active and inactive for each emulated interface.<table>
<tr>
<th> Emulated interface </th>
<th>Active device or immediate context  interfaces </th>
<th>Inactive device or immediate context  interfaces</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> or
                


<a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a> +
                


<a href="https://msdn.microsoft.com/en-us/library/Ff471331(v=VS.85).aspx">IDXGIDevice1</a> +
                


<a href="https://msdn.microsoft.com/en-us/library/Hh404543(v=VS.85).aspx">IDXGIDevice2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173816(v=VS.85).aspx">ID3D10Multithread</a>


</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>
</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1</a> or
                


<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a> +
                


<a href="https://msdn.microsoft.com/en-us/library/Ff471331(v=VS.85).aspx">IDXGIDevice1</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173816(v=VS.85).aspx">ID3D10Multithread</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> (As published by the immediate context. The Direct3D 10 or Microsoft Direct3D 10.1 emulated interface has no effect on deferred contexts.)
                

</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime disables when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476387(v=VS.85).aspx">ClearDepthStencilView</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173538(v=VS.85).aspx">ClearDepthStencilView</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476388(v=VS.85).aspx">ClearRenderTargetView</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173539(v=VS.85).aspx">ClearRenderTargetView</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476389(v=VS.85).aspx">ClearState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173540(v=VS.85).aspx">ClearState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476391(v=VS.85).aspx">ClearUnorderedAccessViewUint</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476390(v=VS.85).aspx">ClearUnorderedAccessViewFloat</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476392(v=VS.85).aspx">CopyResource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">CopyResource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476393(v=VS.85).aspx">CopyStructureCount</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476394(v=VS.85).aspx">CopySubresourceRegion</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173542(v=VS.85).aspx">CopySubresourceRegion</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476395(v=VS.85).aspx">CSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476396(v=VS.85).aspx">CSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476397(v=VS.85).aspx">CSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476398(v=VS.85).aspx">CSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476399(v=VS.85).aspx">CSGetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476400(v=VS.85).aspx">CSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476401(v=VS.85).aspx">CSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476402(v=VS.85).aspx">CSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476403(v=VS.85).aspx">CSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476404(v=VS.85).aspx">CSSetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476405(v=VS.85).aspx">Dispatch</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476406(v=VS.85).aspx">DispatchIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173543(v=VS.85).aspx">CreateBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476407(v=VS.85).aspx">Draw</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173563(v=VS.85).aspx">Draw</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476408(v=VS.85).aspx">DrawAuto</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173564(v=VS.85).aspx">DrawAuto</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476409(v=VS.85).aspx">DrawIndexed</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173565(v=VS.85).aspx">DrawIndexed</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476410(v=VS.85).aspx">DrawIndexedInstanced</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173566(v=VS.85).aspx">DrawIndexedInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476411(v=VS.85).aspx">DrawIndexedInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476412(v=VS.85).aspx">DrawInstanced</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173567(v=VS.85).aspx">DrawInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476413(v=VS.85).aspx">DrawInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476414(v=VS.85).aspx">DSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476415(v=VS.85).aspx">DSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476416(v=VS.85).aspx">DSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476417(v=VS.85).aspx">DSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476418(v=VS.85).aspx">DSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476419(v=VS.85).aspx">DSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476420(v=VS.85).aspx">DSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476421(v=VS.85).aspx">DSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476423(v=VS.85).aspx">ExecuteCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476424(v=VS.85).aspx">FinishCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476425(v=VS.85).aspx">Flush</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173568(v=VS.85).aspx">Flush</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476426(v=VS.85).aspx">GenerateMips</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173569(v=VS.85).aspx">GenerateMips</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476429(v=VS.85).aspx">GetPredication</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173573(v=VS.85).aspx">GetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476430(v=VS.85).aspx">GetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476431(v=VS.85).aspx">GetType</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173575(v=VS.85).aspx">GetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476432(v=VS.85).aspx">GSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173576(v=VS.85).aspx">GSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476433(v=VS.85).aspx">GSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173577(v=VS.85).aspx">GSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476434(v=VS.85).aspx">GSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173578(v=VS.85).aspx">GSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476435(v=VS.85).aspx">GSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173579(v=VS.85).aspx">GSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476436(v=VS.85).aspx">GSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173580(v=VS.85).aspx">GSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476437(v=VS.85).aspx">GSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173581(v=VS.85).aspx">GSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476438(v=VS.85).aspx">GSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173582(v=VS.85).aspx">GSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476439(v=VS.85).aspx">GSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173583(v=VS.85).aspx">GSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476440(v=VS.85).aspx">HSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476441(v=VS.85).aspx">HSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476442(v=VS.85).aspx">HSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476443(v=VS.85).aspx">HSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476445(v=VS.85).aspx">HSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476446(v=VS.85).aspx">HSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476447(v=VS.85).aspx">HSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476448(v=VS.85).aspx">HSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476449(v=VS.85).aspx">IAGetIndexBuffer</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173584(v=VS.85).aspx">IAGetIndexBuffer</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476450(v=VS.85).aspx">IAGetInputLayout</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173585(v=VS.85).aspx">IAGetInputLayout</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476451(v=VS.85).aspx">IAGetPrimitiveTopology</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173586(v=VS.85).aspx">IAGetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Ff476452(v=VS.85).aspx">IAGetVertexBuffers</a>
</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173587(v=VS.85).aspx">IAGetVertexBuffers</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Ff476453(v=VS.85).aspx">IASetIndexBuffer</a>
</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173588(v=VS.85).aspx">IASetIndexBuffer</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Ff476454(v=VS.85).aspx">IASetInputLayout</a>
</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173589(v=VS.85).aspx">IASetInputLayout</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Ff476455(v=VS.85).aspx">IASetPrimitiveTopology</a>
</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173590(v=VS.85).aspx">IASetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Ff476456(v=VS.85).aspx">IASetVertexBuffers</a>
</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173591(v=VS.85).aspx">IASetVertexBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476458(v=VS.85).aspx">OMGetBlendState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173592(v=VS.85).aspx">OMGetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476459(v=VS.85).aspx">OMGetDepthStencilState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173593(v=VS.85).aspx">OMGetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476460(v=VS.85).aspx">OMGetRenderTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173594(v=VS.85).aspx">OMGetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476461(v=VS.85).aspx">OMGetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476462(v=VS.85).aspx">OMSetBlendState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173595(v=VS.85).aspx">OMSetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476463(v=VS.85).aspx">OMSetDepthStencilState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173596(v=VS.85).aspx">OMSetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476464(v=VS.85).aspx">OMSetRenderTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173597(v=VS.85).aspx">OMSetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476465(v=VS.85).aspx">OMSetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476466(v=VS.85).aspx">PSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173599(v=VS.85).aspx">PSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476467(v=VS.85).aspx">PSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173600(v=VS.85).aspx">PSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476468(v=VS.85).aspx">PSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173601(v=VS.85).aspx">PSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476469(v=VS.85).aspx">PSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173602(v=VS.85).aspx">PSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476470(v=VS.85).aspx">PSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173603(v=VS.85).aspx">PSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476471(v=VS.85).aspx">PSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173604(v=VS.85).aspx">PSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476472(v=VS.85).aspx">PSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173605(v=VS.85).aspx">PSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476473(v=VS.85).aspx">PSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173606(v=VS.85).aspx">PSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476474(v=VS.85).aspx">ResolveSubresource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173607(v=VS.85).aspx">ResolveSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476475(v=VS.85).aspx">RSGetScissorRects</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173608(v=VS.85).aspx">RSGetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476476(v=VS.85).aspx">RSGetState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173609(v=VS.85).aspx">RSGetState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476477(v=VS.85).aspx">RSGetViewports</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173610(v=VS.85).aspx">RSGetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476478(v=VS.85).aspx">RSSetScissorRects</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173611(v=VS.85).aspx">RSSetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476479(v=VS.85).aspx">RSSetState</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173612(v=VS.85).aspx">RSSetState</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476480(v=VS.85).aspx">RSSetViewports</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173613(v=VS.85).aspx">RSSetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476481(v=VS.85).aspx">SetPredication</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173615(v=VS.85).aspx">SetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476482(v=VS.85).aspx">SetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173618(v=VS.85).aspx">SetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476483(v=VS.85).aspx">SOGetTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173619(v=VS.85).aspx">SOGetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476484(v=VS.85).aspx">SOSetTargets</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173620(v=VS.85).aspx">SOSetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476486(v=VS.85).aspx">UpdateSubresource</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173621(v=VS.85).aspx">UpdateSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476487(v=VS.85).aspx">VSGetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173622(v=VS.85).aspx">VSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476488(v=VS.85).aspx">VSGetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173623(v=VS.85).aspx">VSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476489(v=VS.85).aspx">VSGetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173624(v=VS.85).aspx">VSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476490(v=VS.85).aspx">VSGetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173625(v=VS.85).aspx">VSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476491(v=VS.85).aspx">VSSetConstantBuffers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173626(v=VS.85).aspx">VSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476492(v=VS.85).aspx">VSSetSamplers</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173627(v=VS.85).aspx">VSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476493(v=VS.85).aspx">VSSetShader</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173628(v=VS.85).aspx">VSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476494(v=VS.85).aspx">VSSetShaderResources</a>


</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173629(v=VS.85).aspx">VSSetShaderResources</a>


</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime does not disable when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476386(v=VS.85).aspx">Begin</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476422(v=VS.85).aspx">End</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173570(v=VS.85).aspx">GetCreationFlags</a>


</td>
</tr>
<tr>
<td></td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173574(v=VS.85).aspx">GetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476427(v=VS.85).aspx">GetContextFlags</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476428(v=VS.85).aspx">GetData</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476457(v=VS.85).aspx">Map</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff476485(v=VS.85).aspx">Unmap</a>


</td>
<td></td>
</tr>
</table>
 



The following table shows the <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a> interface methods that the runtime does not disable because they are not immediate context methods.<table>
<tr>
<th>Methods of <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173534(v=VS.85).aspx">CheckCounter</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173535(v=VS.85).aspx">CheckCounterInfo</a>


</td>
</tr>
<tr>
<td>
Create*, like <a href="https://msdn.microsoft.com/en-us/library/Bb173553(v=VS.85).aspx">CreateQuery</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173571(v=VS.85).aspx">GetDeviceRemovedReason</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173572(v=VS.85).aspx">GetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173598(v=VS.85).aspx">OpenSharedResource</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173614(v=VS.85).aspx">SetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173616(v=VS.85).aspx">SetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Bb173617(v=VS.85).aspx">SetPrivateDataInterface</a>


</td>
</tr>
</table>
 



<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a>
 

 

