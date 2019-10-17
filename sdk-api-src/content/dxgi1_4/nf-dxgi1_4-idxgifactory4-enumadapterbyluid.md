---
UID: NF:dxgi1_4.IDXGIFactory4.EnumAdapterByLuid
title: IDXGIFactory4::EnumAdapterByLuid (dxgi1_4.h)
author: windows-sdk-content
description: Outputs the IDXGIAdapter for the specified LUID.
old-location: direct3ddxgi\idxgifactory4_enumadapterbyluid.htm
tech.root: direct3ddxgi
ms.assetid: AC800F32-2922-45BA-A6D3-D3E45113B9A7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumAdapterByLuid, EnumAdapterByLuid method [DXGI], EnumAdapterByLuid method [DXGI],IDXGIFactory4 interface, IDXGIFactory4 interface [DXGI],EnumAdapterByLuid method, IDXGIFactory4.EnumAdapterByLuid, IDXGIFactory4::EnumAdapterByLuid, direct3ddxgi.idxgifactory4_enumadapterbyluid, dxgi1_4/IDXGIFactory4::EnumAdapterByLuid
ms.topic: method
f1_keywords: 
 - "dxgi1_4/IDXGIFactory4.EnumAdapterByLuid"
dev_langs:
 - c++
req.header: dxgi1_4.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory4.EnumAdapterByLuid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory4::EnumAdapterByLuid


## -description


Outputs the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> for the specified LUID.
        


## -parameters




### -param AdapterLuid [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a></b>

A unique value that identifies the adapter.
            See <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a> for a definition of the structure.
            <b>LUID</b> is defined in dxgi.h.
          


### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.
          


### -param ppvAdapter [out]

Type: <b>void**</b>

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.
          


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.
            See also Direct3D 12 Return Codes.
          




## -remarks



For Direct3D 12, it's no longer possible to backtrack from a device to the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> that was used to create it.
          <b>IDXGIFactory4::EnumAdapterByLuid</b>enables an app to retrieve information about the adapter where a D3D12 device was created.
          <b>IDXGIFactory4::EnumAdapterByLuid</b> is designed to be paired with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getadapterluid">ID3D12Device::GetAdapterLuid</a>.
          For more information, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-1-4-improvements">DXGI 1.4 Improvements</a>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgifactory4">IDXGIFactory4</a>
 

 

