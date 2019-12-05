---
UID: NF:dxgi.IDXGIAdapter.CheckInterfaceSupport
title: IDXGIAdapter::CheckInterfaceSupport (dxgi.h)
description: Checks whether the system supports a device interface for a graphics component.
old-location: direct3ddxgi\idxgiadapter_checkinterfacesupport.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter_checkinterfacesupport.htm
ms.date: 12/05/2018
ms.keywords: 5922d4df-f6ec-4fce-1a94-3779ba7e2830, CheckInterfaceSupport, CheckInterfaceSupport method [DXGI], CheckInterfaceSupport method [DXGI],IDXGIAdapter interface, IDXGIAdapter interface [DXGI],CheckInterfaceSupport method, IDXGIAdapter.CheckInterfaceSupport, IDXGIAdapter::CheckInterfaceSupport, direct3ddxgi.idxgiadapter_checkinterfacesupport, dxgi/IDXGIAdapter::CheckInterfaceSupport
ms.topic: method
f1_keywords:
- dxgi/IDXGIAdapter.CheckInterfaceSupport
dev_langs:
- c++
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
- IDXGIAdapter.CheckInterfaceSupport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIAdapter::CheckInterfaceSupport


## -description


Checks whether the system supports a device interface for a graphics component.


## -parameters




### -param InterfaceName [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

The GUID of the interface of the device version for which support is being checked. For example, __uuidof(ID3D10Device).


### -param pUMDVersion [out]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-large_integer~r1">LARGE_INTEGER</a>*</b>

The user mode driver version of <i>InterfaceName</i>. This is  returned only if the interface is supported, otherwise this parameter will be <b>NULL</b>.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK indicates that the interface is supported, otherwise DXGI_ERROR_UNSUPPORTED is returned (For more information, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>).




## -remarks



<div class="alert"><b>Note</b>  You can  use <b>CheckInterfaceSupport</b> only to  check whether a Direct3D 10.x interface is supported, and only on Windows Vista SP1 and later versions of the operating system. If you try to use <b>CheckInterfaceSupport</b> to check whether a Direct3D 11.x and later version interface is supported, <b>CheckInterfaceSupport</b> returns DXGI_ERROR_UNSUPPORTED. Therefore, do not use <b>CheckInterfaceSupport</b>. Instead, to verify whether the operating system supports a particular interface, try to create the interface. For example, if you call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createblendstate">ID3D11Device::CreateBlendState</a> method and it fails, the operating system does not support the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a> interface.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>
 

 

