---
UID: NF:dxgi.IDXGIDeviceSubObject.GetDevice
title: IDXGIDeviceSubObject::GetDevice (dxgi.h)
description: Retrieves the device.
helpviewer_keywords: ["GetDevice","GetDevice method [DXGI]","GetDevice method [DXGI]","IDXGIDeviceSubObject interface","IDXGIDeviceSubObject interface [DXGI]","GetDevice method","IDXGIDeviceSubObject.GetDevice","IDXGIDeviceSubObject::GetDevice","b3dce65b-334c-0973-c391-77df6912fc77","direct3ddxgi.idxgidevicesubobject_getdevice","dxgi/IDXGIDeviceSubObject::GetDevice"]
old-location: direct3ddxgi\idxgidevicesubobject_getdevice.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevicesubobject_getdevice.htm
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [DXGI], GetDevice method [DXGI],IDXGIDeviceSubObject interface, IDXGIDeviceSubObject interface [DXGI],GetDevice method, IDXGIDeviceSubObject.GetDevice, IDXGIDeviceSubObject::GetDevice, b3dce65b-334c-0973-c391-77df6912fc77, direct3ddxgi.idxgidevicesubobject_getdevice, dxgi/IDXGIDeviceSubObject::GetDevice
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
 - IDXGIDeviceSubObject::GetDevice
 - dxgi/IDXGIDeviceSubObject::GetDevice
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
 - IDXGIDeviceSubObject.GetDevice
---

# IDXGIDeviceSubObject::GetDevice


## -description

Retrieves the device.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The reference id for the device.

### -param ppDevice [out]

Type: <b>void**</b>

The address of a pointer to the device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

A code that indicates success or failure (see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>).

## -remarks

The type of interface that is returned can be any interface published by the device. For example, it could be an IDXGIDevice * called pDevice, and therefore the REFIID would be obtained by calling __uuidof(pDevice).

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>