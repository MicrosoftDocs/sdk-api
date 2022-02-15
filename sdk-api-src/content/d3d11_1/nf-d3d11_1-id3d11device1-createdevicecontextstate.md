---
UID: NF:d3d11_1.ID3D11Device1.CreateDeviceContextState
title: ID3D11Device1::CreateDeviceContextState (d3d11_1.h)
description: Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.
helpviewer_keywords: ["CreateDeviceContextState","CreateDeviceContextState method [Direct3D 11]","CreateDeviceContextState method [Direct3D 11]","ID3D11Device1 interface","ID3D11Device1 interface [Direct3D 11]","CreateDeviceContextState method","ID3D11Device1.CreateDeviceContextState","ID3D11Device1::CreateDeviceContextState","d3d11_1/ID3D11Device1::CreateDeviceContextState","direct3d11.id3d11device1_createdevicecontextstate"]
old-location: direct3d11\id3d11device1_createdevicecontextstate.htm
tech.root: direct3d11
ms.assetid: 8887C3F1-3EA3-4948-A019-E3CB3F3D46C6
ms.date: 12/05/2018
ms.keywords: CreateDeviceContextState, CreateDeviceContextState method [Direct3D 11], CreateDeviceContextState method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateDeviceContextState method, ID3D11Device1.CreateDeviceContextState, ID3D11Device1::CreateDeviceContextState, d3d11_1/ID3D11Device1::CreateDeviceContextState, direct3d11.id3d11device1_createdevicecontextstate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device1::CreateDeviceContextState
 - d3d11_1/ID3D11Device1::CreateDeviceContextState
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
 - ID3D11Device1.CreateDeviceContextState
---

# ID3D11Device1::CreateDeviceContextState


## -description

Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior.

## -parameters

### -param Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of 
              <a href="/windows/desktop/api/d3d11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</a> 
              values that are combined by using a bitwise <b>OR</b> operation. 
              The resulting value specifies how to create the context state object. 
              The 
              <a href="/windows/desktop/api/d3d11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag">D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</a> flag is currently the only defined flag. 
              If the original device was created with 
              <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_SINGLETHREADED</a>, 
              you must create all context state objects from that device with the 
             <b>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED</b> flag.
            



If you set the single-threaded flag for both the context state object and the device, you guarantee that you will call the whole set of context methods and device methods only from one thread. 
            You therefore do not need to use critical sections to synchronize access to the device context, and the runtime can avoid working with those processor-intensive critical sections.

### -param pFeatureLevels [in]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a> values. The array can contain elements from the following list and determines the order of feature levels for which creation is attempted.
              Unlike <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>, you can't set <i>pFeatureLevels</i> to <b>NULL</b> because  there is no default feature level array.
            


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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in <i>pFeatureLevels</i>. Unlike <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>, you must set <i>FeatureLevels</i> to greater than 0 because you can't set <i>pFeatureLevels</i> to <b>NULL</b>.

### -param SDKVersion

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The SDK version. You must set this parameter to <b>D3D11_SDK_VERSION</b>.

### -param EmulatedInterface

Type: <b>REFIID</b>

The globally unique identifier (GUID) for the emulated interface. This value specifies the behavior of the device when the context state object is active. Valid values are  obtained by using the <b>__uuidof</b> operator on the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>, <a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a>, <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>, and <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a> interfaces. See Remarks.

### -param pChosenFeatureLevel [out, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a> value from the <i>pFeatureLevels</i> array. This is the first array value with which <b>CreateDeviceContextState</b> succeeded in creating the context state object. If the call to <b>CreateDeviceContextState</b> fails, the variable pointed to by <i>pChosenFeatureLevel</i> is set to zero.

### -param ppContextState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate">ID3DDeviceContextState</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate">ID3DDeviceContextState</a> object that represents the state of a Direct3D device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The  <b>REFIID</b> value of the emulated interface is a GUID obtained by use of the <b>__uuidof</b> operator. For example, <code>__uuidof(ID3D11Device)</code> gets the GUID of the interface to a Microsoft Direct3D 11 device.
        

Call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate">ID3D11DeviceContext1::SwapDeviceContextState</a> method to activate the context state object. When the context state object is active, the device behaviors that are associated with both the context state object's feature level and its compatible interface are activated on the Direct3D device until the next call to <b>SwapDeviceContextState</b>.
        

When a context state object is active, the runtime disables certain methods on the device and context interfaces. For example, a context state object that is created with <code>__uuidof(ID3D11Device)</code> will cause the runtime to turn off most of the Microsoft Direct3D 10 device interfaces, and a context state object that is created with <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> will cause the runtime to turn off most of the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> methods.
          This behavior ensures that a user of either emulated interface cannot set device state that the other emulated interface is unable to express. This restriction helps guarantee that the <a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a> emulated interface accurately reflects the full state of the pipeline and that the emulated interface will not operate contrary to its original interface definition.
        

For example, suppose the tessellation stage is made active through the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface
          when you create the device through <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>,  instead of through the Direct3D 10 equivalents. Because  the Direct3D 11 context is active, a Direct3D 10 interface is inactive when you first retrieve it via <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. This means that you cannot  immediately pass a Direct3D 10 interface that you retrieved from a Direct3D 11 device to a function. You must first call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate">SwapDeviceContextState</a> to activate a Direct3D 10-compatible context state object.
        

The following table shows the methods that are active and inactive for each emulated interface.<table>
<tr>
<th> Emulated interface </th>
<th>Active device or immediate context  interfaces </th>
<th>Inactive device or immediate context  interfaces</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> or
                


<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>


</td>
<td>

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> +
                


<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a> +
                


<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread</a>


</td>
<td>
<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>
</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a> or
                


<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>



<a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> +
                


<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread</a>


</td>
<td>

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> (As published by the immediate context. The Direct3D 10 or Microsoft Direct3D 10.1 emulated interface has no effect on deferred contexts.)
                

</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime disables when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cleardepthstencilview">ClearDepthStencilView</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-cleardepthstencilview">ClearDepthStencilView</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview">ClearRenderTargetView</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview">ClearRenderTargetView</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ClearState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearstate">ClearState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewuint">ClearUnorderedAccessViewUint</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewfloat">ClearUnorderedAccessViewFloat</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">CopyResource</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">CopyResource</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount">CopyStructureCount</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">CopySubresourceRegion</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copysubresourceregion">CopySubresourceRegion</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetconstantbuffers">CSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetsamplers">CSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetshader">CSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetshaderresources">CSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-csgetunorderedaccessviews">CSGetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetconstantbuffers">CSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetsamplers">CSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetshader">CSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetshaderresources">CSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews">CSSetUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">Dispatch</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect">DispatchIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createblendstate">CreateBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-draw">Draw</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-draw">Draw</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto">DrawAuto</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawauto">DrawAuto</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed">DrawIndexed</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexed">DrawIndexed</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstanced">DrawIndexedInstanced</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexedinstanced">DrawIndexedInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstancedindirect">DrawIndexedInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstanced">DrawInstanced</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawinstanced">DrawInstanced</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstancedindirect">DrawInstancedIndirect</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers">DSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetsamplers">DSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetshader">DSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dsgetshaderresources">DSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers">DSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetsamplers">DSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetshader">DSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetshaderresources">DSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-executecommandlist">ExecuteCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-finishcommandlist">FinishCommandList</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">Flush</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-flush">Flush</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips">GenerateMips</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-generatemips">GenerateMips</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getpredication">GetPredication</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getpredication">GetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getresourceminlod">GetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gettype">GetType</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gettextfiltersize">GetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetconstantbuffers">GSGetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetconstantbuffers">GSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetsamplers">GSGetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetsamplers">GSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetshader">GSGetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetshader">GSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gsgetshaderresources">GSGetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gsgetshaderresources">GSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers">GSSetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetconstantbuffers">GSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetsamplers">GSSetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetsamplers">GSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshader">GSSetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader">GSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshaderresources">GSSetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">GSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers">HSGetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetsamplers">HSGetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetshader">HSGetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hsgetshaderresources">HSGetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers">HSSetConstantBuffers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetsamplers">HSSetSamplers</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetshader">HSSetShader</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetshaderresources">HSSetShaderResources</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetindexbuffer">IAGetIndexBuffer</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetindexbuffer">IAGetIndexBuffer</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetinputlayout">IAGetInputLayout</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetinputlayout">IAGetInputLayout</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetprimitivetopology">IAGetPrimitiveTopology</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetprimitivetopology">IAGetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iagetvertexbuffers">IAGetVertexBuffers</a>
</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iagetvertexbuffers">IAGetVertexBuffers</a>


</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetindexbuffer">IASetIndexBuffer</a>
</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetindexbuffer">IASetIndexBuffer</a>


</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetinputlayout">IASetInputLayout</a>
</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetinputlayout">IASetInputLayout</a>


</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology">IASetPrimitiveTopology</a>
</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetprimitivetopology">IASetPrimitiveTopology</a>


</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers">IASetVertexBuffers</a>
</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetvertexbuffers">IASetVertexBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetblendstate">OMGetBlendState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetblendstate">OMGetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetdepthstencilstate">OMGetDepthStencilState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetdepthstencilstate">OMGetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetrendertargets">OMGetRenderTargets</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omgetrendertargets">OMGetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetrendertargetsandunorderedaccessviews">OMGetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">OMSetBlendState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">OMSetBlendState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate">OMSetDepthStencilState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetdepthstencilstate">OMSetDepthStencilState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">OMSetRenderTargets</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">OMSetRenderTargets</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews">OMSetRenderTargetsAndUnorderedAccessViews</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetconstantbuffers">PSGetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetconstantbuffers">PSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetsamplers">PSGetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetsamplers">PSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetshader">PSGetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetshader">PSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-psgetshaderresources">PSGetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-psgetshaderresources">PSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers">PSSetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetconstantbuffers">PSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetsamplers">PSSetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetsamplers">PSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader">PSSetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader">PSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshaderresources">PSSetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">PSSetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ResolveSubresource</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource">ResolveSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetscissorrects">RSGetScissorRects</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetscissorrects">RSGetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetstate">RSGetState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetstate">RSGetState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rsgetviewports">RSGetViewports</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rsgetviewports">RSGetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetscissorrects">RSSetScissorRects</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetscissorrects">RSSetScissorRects</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">RSSetState</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetstate">RSSetState</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetviewports">RSSetViewports</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetviewports">RSSetViewports</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setpredication">SetPredication</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setpredication">SetPredication</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setresourceminlod">SetResourceMinLOD</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-settextfiltersize">SetTextFilterSize</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sogettargets">SOGetTargets</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-sogettargets">SOGetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sosettargets">SOSetTargets</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-sosettargets">SOSetTargets</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">UpdateSubresource</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-updatesubresource">UpdateSubresource</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetconstantbuffers">VSGetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetconstantbuffers">VSGetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetsamplers">VSGetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetsamplers">VSGetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetshader">VSGetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetshader">VSGetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vsgetshaderresources">VSGetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vsgetshaderresources">VSGetShaderResources</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers">VSSetConstantBuffers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetconstantbuffers">VSSetConstantBuffers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetsamplers">VSSetSamplers</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetsamplers">VSSetSamplers</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshader">VSSetShader</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader">VSSetShader</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">VSSetShaderResources</a>


</td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">VSSetShaderResources</a>


</td>
</tr>
</table>
 



The following table shows the immediate context methods that the runtime does not disable when the indicated context state objects are active.<table>
<tr>
<th>Methods of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> when <code>__uuidof(ID3D10Device1)</code> or <code>__uuidof(ID3D10Device)</code> is active
              </th>
<th>Methods of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a> when <code>__uuidof(ID3D11Device)</code> is active
              </th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">Begin</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">End</a>


</td>
<td></td>
</tr>
<tr>
<td></td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getcreationflags">GetCreationFlags</a>


</td>
</tr>
<tr>
<td></td>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getprivatedata">GetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getcontextflags">GetContextFlags</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">GetData</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a>


</td>
<td></td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-unmap">Unmap</a>


</td>
<td></td>
</tr>
</table>
 



The following table shows the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a> interface methods that the runtime does not disable because they are not immediate context methods.<table>
<tr>
<th>Methods of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounter">CheckCounter</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounterinfo">CheckCounterInfo</a>


</td>
</tr>
<tr>
<td>
Create*, like <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createquery">CreateQuery</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getdeviceremovedreason">GetDeviceRemovedReason</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getexceptionmode">GetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-opensharedresource">OpenSharedResource</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setexceptionmode">SetExceptionMode</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setprivatedata">SetPrivateData</a>


</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setprivatedatainterface">SetPrivateDataInterface</a>


</td>
</tr>
</table>
 



<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>