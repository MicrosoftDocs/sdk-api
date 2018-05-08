---
UID: NF:dxgi.IDXGIAdapter.GetDesc
title: IDXGIAdapter::GetDesc
author: windows-driver-content
description: Gets a DXGI 1.0 description of an adapter (or video card).
old-location: direct3ddxgi\idxgiadapter_getdesc.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter_getdesc.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGIAdapter interface, IDXGIAdapter interface [DXGI],GetDesc method, IDXGIAdapter.GetDesc, IDXGIAdapter::GetDesc, d6097f67-3411-f7d2-50dc-507efce034b7, direct3ddxgi.idxgiadapter_getdesc, dxgi/IDXGIAdapter::GetDesc
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIAdapter.GetDesc
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter::GetDesc


## -description


Gets a DXGI 1.0 description of an adapter (or video card).


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/df39ce37-e1ed-40f3-bfb0-3f7eddf4ec19">DXGI_ADAPTER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/df39ce37-e1ed-40f3-bfb0-3f7eddf4ec19">DXGI_ADAPTER_DESC</a> structure that describes the adapter. This parameter must not be <b>NULL</b>. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <b>GetDesc</b> returns zeros for the PCI ID in the <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of <b>DXGI_ADAPTER_DESC</b> and “Software Adapter” for the description string in the <b>Description</b> member.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.  
        




## -remarks



Graphics apps can use the DXGI API to retrieve an accurate set of graphics memory 
      values on systems that have Windows Display Driver Model (WDDM) drivers. The following are the critical steps involved.

<ul>
<li>
        Graphics driver model determination —
        Because DXGI is only available on systems with WDDM drivers, the app must first confirm the driver model by using the following API.
        <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
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
      </pre>
</td>
</tr>
</table></span></div>
</li>
<li>
      Retrieval of graphics memory values.—

      After the app determines the driver model to be WDDM, the app can use the Direct3D 10 or later API and DXGI to get the amount of graphics memory. 
      After you create a Direct3D device, use this code to obtain 
      a <a href="https://msdn.microsoft.com/df39ce37-e1ed-40f3-bfb0-3f7eddf4ec19">DXGI_ADAPTER_DESC</a> structure that contains the amount of available graphics memory.
      
      <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice), (void **)&amp;pDXGIDevice);
IDXGIAdapter * pDXGIAdapter;
pDXGIDevice-&gt;GetAdapter(&amp;pDXGIAdapter);
DXGI_ADAPTER_DESC adapterDesc;
pDXGIAdapter-&gt;GetDesc(&amp;adapterDesc);
      </pre>
</td>
</tr>
</table></span></div>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>
 

 

