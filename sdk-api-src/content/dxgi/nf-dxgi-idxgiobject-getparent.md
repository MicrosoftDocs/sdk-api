---
UID: NF:dxgi.IDXGIObject.GetParent
title: IDXGIObject::GetParent (dxgi.h)
description: Gets the parent of the object.
helpviewer_keywords: ["0b798351-1afe-ecf7-b14a-ae10203d18e1","GetParent","GetParent method [DXGI]","GetParent method [DXGI]","IDXGIObject interface","IDXGIObject interface [DXGI]","GetParent method","IDXGIObject.GetParent","IDXGIObject::GetParent","direct3ddxgi.idxgiobject_getparent","dxgi/IDXGIObject::GetParent"]
old-location: direct3ddxgi\idxgiobject_getparent.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_getparent.htm
ms.date: 12/05/2018
ms.keywords: 0b798351-1afe-ecf7-b14a-ae10203d18e1, GetParent, GetParent method [DXGI], GetParent method [DXGI],IDXGIObject interface, IDXGIObject interface [DXGI],GetParent method, IDXGIObject.GetParent, IDXGIObject::GetParent, direct3ddxgi.idxgiobject_getparent, dxgi/IDXGIObject::GetParent
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
 - IDXGIObject::GetParent
 - dxgi/IDXGIObject::GetParent
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
 - IDXGIObject.GetParent
---

# IDXGIObject::GetParent


## -description

Gets the parent of the object.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The ID of the requested interface.

### -param ppParent [out]

Type: <b>void**</b>

The address of a pointer to the parent object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>