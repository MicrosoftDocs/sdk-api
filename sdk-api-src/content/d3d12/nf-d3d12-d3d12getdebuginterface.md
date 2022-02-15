---
UID: NF:d3d12.D3D12GetDebugInterface
title: D3D12GetDebugInterface function (d3d12.h)
description: Gets a debug interface.
helpviewer_keywords: ["D3D12GetDebugInterface","D3D12GetDebugInterface function","d3d12/D3D12GetDebugInterface","direct3d12.d3d12getdebuginterface"]
old-location: direct3d12\d3d12getdebuginterface.htm
tech.root: direct3d12
ms.assetid: 6D1D6B73-3C2C-4BE0-B75D-2CD39DAC9499
ms.date: 12/05/2018
ms.keywords: D3D12GetDebugInterface, D3D12GetDebugInterface function, d3d12/D3D12GetDebugInterface, direct3d12.d3d12getdebuginterface
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12GetDebugInterface
 - d3d12/D3D12GetDebugInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12GetDebugInterface
---

# D3D12GetDebugInterface function


## -description

Gets a debug interface.

Use [D3D12GetInterface](nf-d3d12-d3d12getinterface.md) to directly access newer interfaces, especially downlevel.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the debug interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the debug interface can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug">ID3D12Debug</a>) will get the <b>GUID</b> of the debug interface.

### -param ppvDebug [out, optional]

Type: <b>void**</b>

The debug interface, as a pointer to pointer to void.
            See
            <a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug">ID3D12Debug</a> and
            <a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice">ID3D12DebugDevice</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

The function signature PFN_D3D12_GET_DEBUG_INTERFACE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      


#### Examples

Enable the D3D12 debug layer.


```cpp
// Enable the D3D12 debug layer.
{
    
    ComPtr<ID3D12Debug> debugController;
    if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
    {
        debugController->EnableDebugLayer();
    }
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>