---
UID: NF:dxgi.IDXGIObject.GetPrivateData
title: IDXGIObject::GetPrivateData (dxgi.h)
description: Get a pointer to the object's data.
helpviewer_keywords: ["86763938-a2bf-a817-2ffc-645427783675","GetPrivateData","GetPrivateData method [DXGI]","GetPrivateData method [DXGI]","IDXGIObject interface","IDXGIObject interface [DXGI]","GetPrivateData method","IDXGIObject.GetPrivateData","IDXGIObject::GetPrivateData","direct3ddxgi.idxgiobject_getprivatedata","dxgi/IDXGIObject::GetPrivateData"]
old-location: direct3ddxgi\idxgiobject_getprivatedata.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_getprivatedata.htm
ms.date: 12/05/2018
ms.keywords: 86763938-a2bf-a817-2ffc-645427783675, GetPrivateData, GetPrivateData method [DXGI], GetPrivateData method [DXGI],IDXGIObject interface, IDXGIObject interface [DXGI],GetPrivateData method, IDXGIObject.GetPrivateData, IDXGIObject::GetPrivateData, direct3ddxgi.idxgiobject_getprivatedata, dxgi/IDXGIObject::GetPrivateData
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
 - IDXGIObject::GetPrivateData
 - dxgi/IDXGIObject::GetPrivateData
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
 - IDXGIObject.GetPrivateData
---

# IDXGIObject::GetPrivateData


## -description

Get a pointer to the object's data.

## -parameters

### -param Name [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

A GUID identifying the data.

### -param pDataSize [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

The size of the data.

### -param pData [out]

Type: <b>void*</b>

Pointer to the data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

If the data returned is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or one of its derivative classes, previously set by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-setprivatedatainterface">IDXGIObject::SetPrivateDataInterface</a>, you must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">::Release()</a> on the pointer before the pointer is freed to decrement the reference count.

You can pass <b>GUID_DeviceType</b> in the <i>Name</i> parameter of <b>GetPrivateData</b> to retrieve the device type from the display adapter object (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>, <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>, <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiadapter2">IDXGIAdapter2</a>). 

<p class="proch"><b>To get the type of device on which the display adapter was created</b>

<ol>
<li>Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> or <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a> object to retrieve the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> object.</li>
<li>Call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">GetParent</a> on the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> object to retrieve the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> object.</li>
<li>Call <b>GetPrivateData</b> on the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> object with <b>GUID_DeviceType</b> to retrieve the type of device on which the display adapter was created. <i>pData</i> will point to a value from the driver-type enumeration (for example, a value from <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a>).</li>
</ol>
On Windows 7 or earlier, this type is either a value from <a href="/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a> or <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a> depending on which kind of device was created. On Windows 8, this type is always a value from <b>D3D_DRIVER_TYPE</b>. Don't use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-setprivatedata">IDXGIObject::SetPrivateData</a> with <b>GUID_DeviceType</b> because the behavior when doing so is undefined.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>