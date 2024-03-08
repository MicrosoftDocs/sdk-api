---
UID: NF:dxgi.IDXGIAdapter1.GetDesc1
title: IDXGIAdapter1::GetDesc1 (dxgi.h)
description: Gets a DXGI 1.1 description of an adapter (or video card).
helpviewer_keywords: ["GetDesc1","GetDesc1 method [DXGI]","GetDesc1 method [DXGI]","IDXGIAdapter1 interface","IDXGIAdapter1 interface [DXGI]","GetDesc1 method","IDXGIAdapter1.GetDesc1","IDXGIAdapter1::GetDesc1","b985f570-96ae-e1c8-11c4-3485b12285bc","direct3ddxgi.idxgiadapter1_getdesc1","dxgi/IDXGIAdapter1::GetDesc1"]
old-location: direct3ddxgi\idxgiadapter1_getdesc1.htm
tech.root: direct3ddxgi
ms.assetid: 1eb051f8-4e64-41fe-8177-6aad47714cb9
ms.date: 12/05/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGIAdapter1 interface, IDXGIAdapter1 interface [DXGI],GetDesc1 method, IDXGIAdapter1.GetDesc1, IDXGIAdapter1::GetDesc1, b985f570-96ae-e1c8-11c4-3485b12285bc, direct3ddxgi.idxgiadapter1_getdesc1, dxgi/IDXGIAdapter1::GetDesc1
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIAdapter1::GetDesc1
 - dxgi/IDXGIAdapter1::GetDesc1
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
 - IDXGIAdapter1.GetDesc1
---

# IDXGIAdapter1::GetDesc1


## -description

Gets a DXGI 1.1 description of an adapter (or video card).

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc1">DXGI_ADAPTER_DESC1</a>*</b>

A pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc1">DXGI_ADAPTER_DESC1</a> structure that describes the adapter.  
      This parameter must not be <b>NULL</b>. On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9 graphics hardware, <b>GetDesc1</b> returns zeros for <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of <b>DXGI_ADAPTER_DESC1</b> and “Software Adapter” for the description string in the <b>Description</b> member.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

Use the <b>GetDesc1</b> method to get a DXGI 1.1 description of an adapter.  To get a DXGI 1.0 description, use the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">IDXGIAdapter::GetDesc</a>