---
UID: NF:dxgi.IDXGIDevice.QueryResourceResidency
title: IDXGIDevice::QueryResourceResidency (dxgi.h)
description: Gets the residency status of an array of resources.
helpviewer_keywords: ["0f2dfe96-267a-14d2-b7ec-deb2ed3c3450","IDXGIDevice interface [DXGI]","QueryResourceResidency method","IDXGIDevice.QueryResourceResidency","IDXGIDevice::QueryResourceResidency","QueryResourceResidency","QueryResourceResidency method [DXGI]","QueryResourceResidency method [DXGI]","IDXGIDevice interface","direct3ddxgi.idxgidevice_queryresourceresidency","dxgi/IDXGIDevice::QueryResourceResidency"]
old-location: direct3ddxgi\idxgidevice_queryresourceresidency.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_queryresourceresidency.htm
ms.date: 12/05/2018
ms.keywords: 0f2dfe96-267a-14d2-b7ec-deb2ed3c3450, IDXGIDevice interface [DXGI],QueryResourceResidency method, IDXGIDevice.QueryResourceResidency, IDXGIDevice::QueryResourceResidency, QueryResourceResidency, QueryResourceResidency method [DXGI], QueryResourceResidency method [DXGI],IDXGIDevice interface, direct3ddxgi.idxgidevice_queryresourceresidency, dxgi/IDXGIDevice::QueryResourceResidency
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
 - IDXGIDevice::QueryResourceResidency
 - dxgi/IDXGIDevice::QueryResourceResidency
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
 - IDXGIDevice.QueryResourceResidency
---

# IDXGIDevice::QueryResourceResidency


## -description

Gets the residency status of an array of resources.

## -parameters

### -param ppResources [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

An array of <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interfaces.

### -param pResidencyStatus [out]

Type: <b><a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency">DXGI_RESIDENCY</a>*</b>

An array of <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency">DXGI_RESIDENCY</a> flags. Each element describes the residency status for corresponding element in 
        the <i>ppResources</i> argument array.

### -param NumResources

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of resources in the <i>ppResources</i> argument array and <i>pResidencyStatus</i> argument array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_DEVICE_REMOVED</a>, E_INVALIDARG, or 
      E_POINTER (see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a> and WinError.h for more information).

## -remarks

The information returned by the <i>pResidencyStatus</i> argument array describes the residency status at the time that the <b>QueryResourceResidency</b> method was called.  
      

<div class="alert"><b>Note</b>  The residency status will constantly change.</div>
<div> </div>
If you call the <b>QueryResourceResidency</b> method during a device removed state, the <i>pResidencyStatus</i> argument will return the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency">DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY</a> flag.

<div class="alert"><b>Note</b>  This method should not be called every frame as it incurs a non-trivial amount of overhead.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>