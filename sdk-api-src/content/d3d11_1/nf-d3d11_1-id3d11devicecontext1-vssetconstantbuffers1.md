---
UID: NF:d3d11_1.ID3D11DeviceContext1.VSSetConstantBuffers1
title: ID3D11DeviceContext1::VSSetConstantBuffers1 (d3d11_1.h)
description: Sets the constant buffers that the vertex shader pipeline stage uses.helpviewer_keywords: ["ID3D11DeviceContext1 interface [Direct3D 11]","VSSetConstantBuffers1 method","ID3D11DeviceContext1.VSSetConstantBuffers1","ID3D11DeviceContext1::VSSetConstantBuffers1","VSSetConstantBuffers1","VSSetConstantBuffers1 method [Direct3D 11]","VSSetConstantBuffers1 method [Direct3D 11]","ID3D11DeviceContext1 interface","d3d11_1/ID3D11DeviceContext1::VSSetConstantBuffers1","direct3d11.id3d11devicecontext1_vssetconstantbuffers1"]
old-location: direct3d11\id3d11devicecontext1_vssetconstantbuffers1.htm
tech.root: direct3d11
ms.assetid: 4D896539-216F-4823-B36E-2FE3E8A40C64
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext1 interface [Direct3D 11],VSSetConstantBuffers1 method, ID3D11DeviceContext1.VSSetConstantBuffers1, ID3D11DeviceContext1::VSSetConstantBuffers1, VSSetConstantBuffers1, VSSetConstantBuffers1 method [Direct3D 11], VSSetConstantBuffers1 method [Direct3D 11],ID3D11DeviceContext1 interface, d3d11_1/ID3D11DeviceContext1::VSSetConstantBuffers1, direct3d11.id3d11devicecontext1_vssetconstantbuffers1
f1_keywords:
- d3d11_1/ID3D11DeviceContext1.VSSetConstantBuffers1
dev_langs:
- c++
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
- ID3D11DeviceContext1.VSSetConstantBuffers1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext1::VSSetConstantBuffers1


## -description


Sets the constant buffers that the vertex shader pipeline stage uses.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting constant buffers to (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - 1).


### -param NumBuffers [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to set (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - <i>StartSlot</i>).


### -param ppConstantBuffers [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

Array of constant buffers being given to the device.


### -param pFirstConstant [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array that holds the offsets into the buffers that  <i>ppConstantBuffers</i> specifies. Each offset specifies where, from the shader's point of view, each constant buffer starts.  Each offset is measured in shader constants, which are 16 bytes (4*32-bit components).  Therefore, an offset of 16 indicates that the start of the associated constant buffer is 256 bytes into the constant buffer. Each offset must be a multiple of 16 constants.


### -param pNumConstants [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array that holds the numbers of constants in the buffers that  <i>ppConstantBuffers</i> specifies. Each number specifies the number of constants that are contained in the constant buffer that the shader uses. Each number of constants starts from its respective offset that is specified in the <i>pFirstConstant</i> array. Each number of constants must be a multiple of 16 constants, in the range [0..4096]. 


## -remarks



The runtime drops the call to <b>VSSetConstantBuffers1</b> if the number of constants to which <i>pNumConstants</i> points is larger than the maximum constant buffer size that is supported by shaders (4096 constants).  The values in the elements of the <i>pFirstConstant</i> and <i>pFirstConstant</i> + <i>pNumConstants</i> arrays can exceed the length of each buffer; from the shader's point of view, the constant buffer is the intersection of the actual memory allocation for the buffer and the window [value in an element of <i>pFirstConstant</i>, value in an element of <i>pFirstConstant</i> + value in an element of <i>pNumConstants</i>]. The runtime also drops the call to <b>VSSetConstantBuffers1</b> on existing drivers that don't support this offsetting.

The runtime will emulate this feature for <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.1, 9.2, and 9.3; therefore, this feature is supported for feature level 9.1, 9.2, and 9.3.  This feature is always available on new drivers for feature level 10 and higher.

From the shader’s point of view, element [0] in the constant buffers array is the constant at <i>pFirstConstant</i>.

Out of bounds access to the constant buffers from the shader to the range that is defined by <i>pFirstConstant</i> and <i>pNumConstants</i> returns 0. 

If <i>pFirstConstant</i> and <i>pNumConstants</i> arrays are <b>NULL</b>, you get the same result as if you were binding the entire buffer into view.  You get this same result if you call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers">VSSetConstantBuffers</a> method. If the buffer is larger than the maximum constant buffer size that is supported by shaders (4096 elements), the shader can access only the first 4096 constants.

If either <i>pFirstConstant</i> or <i>pNumConstants</i> is <b>NULL</b>, the other parameter must also be <b>NULL</b>.

<h3><a id="Calling_VSSetConstantBuffers1_with_command_list_emulation"></a><a id="calling_vssetconstantbuffers1_with_command_list_emulation"></a><a id="CALLING_VSSETCONSTANTBUFFERS1_WITH_COMMAND_LIST_EMULATION"></a>Calling VSSetConstantBuffers1 with command list emulation</h3>
The runtime's <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command list</a> emulation of <b>VSSetConstantBuffers1</b> sometimes doesn't actually change the offsets or sizes for the arrays of constant buffers. This behavior occurs when 

<b>VSSetConstantBuffers1</b> doesn't effectively change the constant buffers at the beginning and end of the range of slots that you set to update. This section shows how to work around this 

behavior.

Here is the code to check whether either the runtime emulates command lists or the driver supports command lists:



```cpp

     HRESULT hr = S_OK;
     bool needWorkaround = false;
     D3D11_DEVICE_CONTEXT_TYPE contextType = pDeviceContext->GetType();

     if( D3D11_DEVICE_CONTEXT_DEFERRED == contextType)
     {
          D3D11_FEATURE_DATA_THREADING threadingCaps = { FALSE, FALSE };

          hr = pDevice->CheckFeatureSupport( D3D11_FEATURE_THREADING, &threadingCaps, sizeof(threadingCaps) );
          if( SUCCEEDED(hr) && !threadingCaps.DriverCommandLists )
          {
               needWorkaround = true; // the runtime emulates command lists.
          }
     }

```


If the runtime emulates command lists, you need to use one of these code snippets:


If you change the offset and size on only a single constant buffer, set the constant buffer to <b>NULL</b> first:



```cpp

     pDeviceContext->VSSetConstantBuffers1(0, 1, &CBuf, &Offset, &Count);
     if( needWorkaround )
     {
          // Workaround for command list emulation
          pDeviceContext->VSSetConstantBuffers(0, 1, &NullCBuf);
     }
     pDeviceContext->VSSetConstantBuffers1(0, 1, &CBuf, &Offset, &Count);

```


If you change multiple constant buffers, set the first and last constant buffers of the range to <b>NULL</b> first:



```cpp

     pDeviceContext->VSSetConstantBuffers1(0, 4, &CBufs, &Offsets, &Counts);
     if( needWorkaround )
     {
          // Workaround for command list emulation
          pDeviceContext->VSSetConstantBuffers(0, 1, &NullCBuf);
          pDeviceContext->VSSetConstantBuffers(3, 1, &NullCBuf);
     }
     pDeviceContext->VSSetConstantBuffers1(0, 4, &CBufs, &Offsets, &Counts);

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>
 

 

