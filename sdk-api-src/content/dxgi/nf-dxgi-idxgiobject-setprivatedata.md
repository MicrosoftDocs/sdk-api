---
UID: NF:dxgi.IDXGIObject.SetPrivateData
title: IDXGIObject::SetPrivateData (dxgi.h)
description: Sets application-defined data to the object and associates that data with a GUID.
helpviewer_keywords: ["5949633e-2d65-5d04-b6ba-29414dfded94","IDXGIObject interface [DXGI]","SetPrivateData method","IDXGIObject.SetPrivateData","IDXGIObject::SetPrivateData","SetPrivateData","SetPrivateData method [DXGI]","SetPrivateData method [DXGI]","IDXGIObject interface","direct3ddxgi.idxgiobject_setprivatedata","dxgi/IDXGIObject::SetPrivateData"]
old-location: direct3ddxgi\idxgiobject_setprivatedata.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_setprivatedata.htm
ms.date: 12/05/2018
ms.keywords: 5949633e-2d65-5d04-b6ba-29414dfded94, IDXGIObject interface [DXGI],SetPrivateData method, IDXGIObject.SetPrivateData, IDXGIObject::SetPrivateData, SetPrivateData, SetPrivateData method [DXGI], SetPrivateData method [DXGI],IDXGIObject interface, direct3ddxgi.idxgiobject_setprivatedata, dxgi/IDXGIObject::SetPrivateData
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
 - IDXGIObject::SetPrivateData
 - dxgi/IDXGIObject::SetPrivateData
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
 - IDXGIObject.SetPrivateData
---

# IDXGIObject::SetPrivateData


## -description

Sets application-defined data to the object and associates that data with a GUID.

## -parameters

### -param Name [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

A GUID that identifies the data. Use this GUID in a call to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getprivatedata">GetPrivateData</a> to get the data.

### -param DataSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the object's data.

### -param pData [in]

Type: <b>const void*</b>

A pointer to the object's data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<b>SetPrivateData</b> makes a copy of the specified data and stores it with the object.

Private data that <b>SetPrivateData</b> stores in the object occupies the same storage space as private data that is stored by associated Direct3D objects (for example, by a Microsoft Direct3D 11 device through <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-setprivatedata">ID3D11Device::SetPrivateData</a> or by a Direct3D 11 child device through <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicechild-setprivatedata">ID3D11DeviceChild::SetPrivateData</a>).

The <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> reports memory leaks by outputting a list of object interface pointers along with their friendly names. The default friendly name is "&lt;unnamed&gt;". You can set the friendly name so that you can determine if the corresponding object interface pointer caused the leak. To set the friendly name, use the <b>SetPrivateData</b> method and the well-known private data GUID (<b>WKPDID_D3DDebugObjectName</b>) that is in D3Dcommon.h. For example, to give pContext a friendly name of <i>My name</i>, use the following code:


```

static const char c_szName[] = "My name";
hr = pContext->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );

```


You can use <b>WKPDID_D3DDebugObjectName</b> to track down memory leaks and understand performance characteristics of your applications. This information is reflected in the output of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> that is related to memory leaks (<a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-reportlivedeviceobjects">ID3D11Debug::ReportLiveDeviceObjects</a>) and with the <a href="/windows/desktop/direct3d11/direct3d-11-1-features">event tracing</a> for Windows events that we've added to Windows 8.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>