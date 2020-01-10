---
UID: NF:dxgi.IDXGIObject.SetPrivateDataInterface
title: IDXGIObject::SetPrivateDataInterface (dxgi.h)
description: Set an interface in the object's private data.
old-location: direct3ddxgi\idxgiobject_setprivatedatainterface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_setprivatedatainterface.htm
ms.date: 12/05/2018
ms.keywords: 37e6a4f2-50a5-efad-af10-20e8f1d053e2, IDXGIObject interface [DXGI],SetPrivateDataInterface method, IDXGIObject.SetPrivateDataInterface, IDXGIObject::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [DXGI], SetPrivateDataInterface method [DXGI],IDXGIObject interface, direct3ddxgi.idxgiobject_setprivatedatainterface, dxgi/IDXGIObject::SetPrivateDataInterface
f1_keywords:
- dxgi/IDXGIObject.SetPrivateDataInterface
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
- IDXGIObject.SetPrivateDataInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIObject::SetPrivateDataInterface


## -description


Set an interface in the object's private data.


## -parameters




### -param Name [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

A GUID identifying the interface.


### -param pUnknown [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The interface to set.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



This API associates an interface pointer with the object.

When the interface is set its reference count is incremented. When the data are overwritten (by calling SPD or SPDI with the same GUID) or the object is destroyed, ::Release() is called and the interface's reference count is decremented.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
 

 

