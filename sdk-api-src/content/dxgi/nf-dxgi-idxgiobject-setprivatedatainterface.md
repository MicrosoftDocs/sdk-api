---
UID: NF:dxgi.IDXGIObject.SetPrivateDataInterface
title: IDXGIObject::SetPrivateDataInterface (dxgi.h)
description: Set an interface in the object's private data.
helpviewer_keywords: ["37e6a4f2-50a5-efad-af10-20e8f1d053e2","IDXGIObject interface [DXGI]","SetPrivateDataInterface method","IDXGIObject.SetPrivateDataInterface","IDXGIObject::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method [DXGI]","SetPrivateDataInterface method [DXGI]","IDXGIObject interface","direct3ddxgi.idxgiobject_setprivatedatainterface","dxgi/IDXGIObject::SetPrivateDataInterface"]
old-location: direct3ddxgi\idxgiobject_setprivatedatainterface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_setprivatedatainterface.htm
ms.date: 12/05/2018
ms.keywords: 37e6a4f2-50a5-efad-af10-20e8f1d053e2, IDXGIObject interface [DXGI],SetPrivateDataInterface method, IDXGIObject.SetPrivateDataInterface, IDXGIObject::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [DXGI], SetPrivateDataInterface method [DXGI],IDXGIObject interface, direct3ddxgi.idxgiobject_setprivatedatainterface, dxgi/IDXGIObject::SetPrivateDataInterface
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
 - IDXGIObject::SetPrivateDataInterface
 - dxgi/IDXGIObject::SetPrivateDataInterface
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
 - IDXGIObject.SetPrivateDataInterface
---

# IDXGIObject::SetPrivateDataInterface


## -description

Set an interface in the object's private data.

## -parameters

### -param Name [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

A GUID identifying the interface.

### -param pUnknown [in]

Type: <b>const <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)-derived interface to be associated with the device object. Its reference count is incremented when set, and decremented when either the [IDXGIObject](/windows/win32/api/dxgi/nn-dxgi-idxgiobject) is destroyed, or when the data is overwritten by calling [SetPrivateData](/windows/win32/api/dxgi/nf-dxgi-idxgiobject-setprivatedata) or **SetPrivateDataInterface** with the same **GUID**.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>