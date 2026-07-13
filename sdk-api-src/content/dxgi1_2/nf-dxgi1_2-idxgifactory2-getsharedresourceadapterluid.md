---
UID: NF:dxgi1_2.IDXGIFactory2.GetSharedResourceAdapterLuid
title: IDXGIFactory2::GetSharedResourceAdapterLuid (dxgi1_2.h)
description: Identifies the adapter on which a shared resource object was created.
helpviewer_keywords: ["GetSharedResourceAdapterLuid","GetSharedResourceAdapterLuid method [DXGI]","GetSharedResourceAdapterLuid method [DXGI]","IDXGIFactory2 interface","IDXGIFactory2 interface [DXGI]","GetSharedResourceAdapterLuid method","IDXGIFactory2.GetSharedResourceAdapterLuid","IDXGIFactory2::GetSharedResourceAdapterLuid","direct3ddxgi.idxgifactory2_getsharedresourceadapterluid","dxgi1_2/IDXGIFactory2::GetSharedResourceAdapterLuid"]
old-location: direct3ddxgi\idxgifactory2_getsharedresourceadapterluid.htm
tech.root: direct3ddxgi
ms.assetid: 278F1C2B-6DE7-4D4A-8C6E-10B1004B8EFC
ms.date: 12/05/2018
ms.keywords: GetSharedResourceAdapterLuid, GetSharedResourceAdapterLuid method [DXGI], GetSharedResourceAdapterLuid method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],GetSharedResourceAdapterLuid method, IDXGIFactory2.GetSharedResourceAdapterLuid, IDXGIFactory2::GetSharedResourceAdapterLuid, direct3ddxgi.idxgifactory2_getsharedresourceadapterluid, dxgi1_2/IDXGIFactory2::GetSharedResourceAdapterLuid
req.header: dxgi1_2.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory2::GetSharedResourceAdapterLuid
 - dxgi1_2/IDXGIFactory2::GetSharedResourceAdapterLuid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.GetSharedResourceAdapterLuid
---

# IDXGIFactory2::GetSharedResourceAdapterLuid


## -description

Identifies the adapter on which a shared resource object was created.

## -parameters

### -param hResource [in]

A handle to a shared resource object. The <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle">IDXGIResource1::CreateSharedHandle</a> method returns this handle.

### -param pLuid [out]

A pointer to a variable that receives a locally unique identifier (<a href="/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a>) value that identifies the adapter. <b>LUID</b> is defined in Dxgi.h. An <b>LUID</b> is a 64-bit value that is guaranteed to be unique only on the operating system on which it was generated. The uniqueness of an <b>LUID</b> is guaranteed only until the operating system is restarted.

## -returns

<b>GetSharedResourceAdapterLuid</b> returns:
        <ul>
<li>S_OK if it  identified the adapter.</li>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>hResource</i> is invalid.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>GetSharedResourceAdapterLuid</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

You cannot share resources across adapters. Therefore, you cannot open a shared resource on an adapter other than the adapter on which the resource was created.  Call <b>GetSharedResourceAdapterLuid</b> before you open a shared resource to ensure that the resource was created on the appropriate adapter. To open a shared resource, call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1">ID3D11Device1::OpenSharedResource1</a> or <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname">ID3D11Device1::OpenSharedResourceByName</a> method.


#### Examples


``` syntax
HANDLE handle;
IDXGIFactory2* pFactory;

LUID luid;
pFactory->GetSharedResourceAdapterLuid (handle, &luid);

UINT index = 0;
IDXGIAdapter* pAdapter = NULL;
while (SUCCEEDED(pFactory->EnumAdapters(index, &pAdapter)))
{
    DXGI_ADAPTER_DESC desc;
    pAdapter->GetDesc(&desc);
    if (desc.AdapterLuid == luid)
    {
       // Identified a matching adapter.
       break;
    }
    pAdapter->Release();
    pAdapter = NULL;
    index++;
}
// At this point, if pAdapter is non-null, you identified an adapter that 
// can open the shared resource.

```


## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>
