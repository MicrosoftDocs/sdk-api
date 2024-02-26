---
UID: NF:dxgi.IDXGIAdapter.GetDesc
title: IDXGIAdapter::GetDesc (dxgi.h)
description: Gets a DXGI 1.0 description of an adapter (or video card).
helpviewer_keywords: ["GetDesc","GetDesc method [DXGI]","GetDesc method [DXGI]","IDXGIAdapter interface","IDXGIAdapter interface [DXGI]","GetDesc method","IDXGIAdapter.GetDesc","IDXGIAdapter::GetDesc","d6097f67-3411-f7d2-50dc-507efce034b7","direct3ddxgi.idxgiadapter_getdesc","dxgi/IDXGIAdapter::GetDesc"]
old-location: direct3ddxgi\idxgiadapter_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter_getdesc.htm
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGIAdapter interface, IDXGIAdapter interface [DXGI],GetDesc method, IDXGIAdapter.GetDesc, IDXGIAdapter::GetDesc, d6097f67-3411-f7d2-50dc-507efce034b7, direct3ddxgi.idxgiadapter_getdesc, dxgi/IDXGIAdapter::GetDesc
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
 - IDXGIAdapter::GetDesc
 - dxgi/IDXGIAdapter::GetDesc
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
 - IDXGIAdapter.GetDesc
---

# IDXGIAdapter::GetDesc


## -description

Gets a DXGI 1.0 description of an adapter (or video card).

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc">DXGI_ADAPTER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc">DXGI_ADAPTER_DESC</a> structure that describes the adapter. This parameter must not be <b>NULL</b>. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <b>GetDesc</b> returns zeros for <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of <b>DXGI_ADAPTER_DESC</b> and “Software Adapter” for the description string in the <b>Description</b> member.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.

## -remarks

Graphics apps can use the DXGI API to retrieve an accurate set of graphics memory 
      values on systems that have Windows Display Driver Model (WDDM) drivers. The following are the critical steps involved.

<ul>
<li>
Graphics driver model determination —Because DXGI is only available on systems with WDDM drivers, the app must first confirm the driver model by using the following API.


```

HasWDDMDriver()
{
    LPDIRECT3DCREATE9EX pD3D9Create9Ex = NULL;
    HMODULE             hD3D9          = NULL;

    hD3D9 = LoadLibrary( L"d3d9.dll" );

    if ( NULL == hD3D9 ) {
        return false;
    }

    //
    /*  Try to create IDirect3D9Ex interface (also known as a DX9L interface). This interface can only be created if the driver is a WDDM driver.
	 */
    //
    pD3D9Create9Ex = (LPDIRECT3DCREATE9EX) GetProcAddress( hD3D9, "Direct3DCreate9Ex" );

    return pD3D9Create9Ex != NULL;
}
      
```


</li>
<li>
Retrieval of graphics memory values.—After the app determines the driver model to be WDDM, the app can use the Direct3D 10 or later API and DXGI to get the amount of graphics memory. 
      After you create a Direct3D device, use this code to obtain 
      a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc">DXGI_ADAPTER_DESC</a> structure that contains the amount of available graphics memory.


```

IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);
IDXGIAdapter * pDXGIAdapter;
pDXGIDevice->GetAdapter(&pDXGIAdapter);
DXGI_ADAPTER_DESC adapterDesc;
pDXGIAdapter->GetDesc(&adapterDesc);
      
```


</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>