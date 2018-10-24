---
UID: NF:dxgi.IDXGIAdapter.EnumOutputs
title: IDXGIAdapter::EnumOutputs
author: windows-sdk-content
description: Enumerate adapter (video card) outputs.
old-location: direct3ddxgi\idxgiadapter_enumoutputs.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter_enumoutputs.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 7da8b512-df54-dc59-9b13-fb6ef2f60fd6, EnumOutputs, EnumOutputs method [DXGI], EnumOutputs method [DXGI],IDXGIAdapter interface, IDXGIAdapter interface [DXGI],EnumOutputs method, IDXGIAdapter.EnumOutputs, IDXGIAdapter::EnumOutputs, direct3ddxgi.idxgiadapter_enumoutputs, dxgi/IDXGIAdapter::EnumOutputs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter::EnumOutputs


## -description


Enumerate adapter (video card) outputs.


## -parameters




### -param Output

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the output.


### -param ppOutput [out]

Type: <b><a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> interface at the position specified by the <i>Output</i> parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

A code that indicates success or failure (see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>). DXGI_ERROR_NOT_FOUND is returned if the index is greater than the number of outputs.

If the adapter came from a device created using D3D_DRIVER_TYPE_WARP, then the adapter has no outputs, so DXGI_ERROR_NOT_FOUND is returned.





## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="dxgi_error.htm">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
When the <b>EnumOutputs</b> method succeeds and fills the <i>ppOutput</i> parameter with the address of the pointer to the output interface, <b>EnumOutputs</b> increments the output interface's reference count. To avoid a memory leak, when you finish using the 
      output interface, call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to decrement the reference count.

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




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>
 

 

