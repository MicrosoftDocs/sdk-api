---
UID: NF:dxgi.IDXGIAdapter.EnumOutputs
title: IDXGIAdapter::EnumOutputs (dxgi.h)
description: Enumerate adapter (video card) outputs.
helpviewer_keywords: ["7da8b512-df54-dc59-9b13-fb6ef2f60fd6","EnumOutputs","EnumOutputs method [DXGI]","EnumOutputs method [DXGI]","IDXGIAdapter interface","IDXGIAdapter interface [DXGI]","EnumOutputs method","IDXGIAdapter.EnumOutputs","IDXGIAdapter::EnumOutputs","direct3ddxgi.idxgiadapter_enumoutputs","dxgi/IDXGIAdapter::EnumOutputs"]
old-location: direct3ddxgi\idxgiadapter_enumoutputs.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter_enumoutputs.htm
ms.date: 12/05/2018
ms.keywords: 7da8b512-df54-dc59-9b13-fb6ef2f60fd6, EnumOutputs, EnumOutputs method [DXGI], EnumOutputs method [DXGI],IDXGIAdapter interface, IDXGIAdapter interface [DXGI],EnumOutputs method, IDXGIAdapter.EnumOutputs, IDXGIAdapter::EnumOutputs, direct3ddxgi.idxgiadapter_enumoutputs, dxgi/IDXGIAdapter::EnumOutputs
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter::EnumOutputs
 - dxgi/IDXGIAdapter::EnumOutputs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIAdapter.EnumOutputs
---

# IDXGIAdapter::EnumOutputs


## -description

Enumerate adapter (video card) outputs.

## -parameters

### -param Output

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the output.

### -param ppOutput [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface at the position specified by the <i>Output</i> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

A code that indicates success or failure (see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>). DXGI_ERROR_NOT_FOUND is returned if the index is greater than the number of outputs.

If the adapter came from a device created using D3D_DRIVER_TYPE_WARP, then the adapter has no outputs, so DXGI_ERROR_NOT_FOUND is returned.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
When the <b>EnumOutputs</b> method succeeds and fills the <i>ppOutput</i> parameter with the address of the pointer to the output interface, <b>EnumOutputs</b> increments the output interface's reference count. To avoid a memory leak, when you finish using the 
      output interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to decrement the reference count.

<b>EnumOutputs</b> first returns the output on which the desktop primary is displayed. This output corresponds with an index of zero. <b>EnumOutputs</b> then returns other outputs.


#### Examples

Enumerating Outputs
          

Here is an example of how to use <b>EnumOutputs</b> to enumerate all the outputs on an adapter:


```

UINT i = 0;
IDXGIOutput * pOutput;
std::vector<IDXGIOutput*> vOutputs;
while(pAdapter->EnumOutputs(i, &pOutput) != DXGI_ERROR_NOT_FOUND)
{
    vOutputs.push_back(pOutput);
    ++i;
}

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>