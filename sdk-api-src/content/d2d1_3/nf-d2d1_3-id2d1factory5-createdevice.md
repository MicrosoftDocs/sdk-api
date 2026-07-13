---
UID: NF:d2d1_3.ID2D1Factory5.CreateDevice
title: ID2D1Factory5::CreateDevice (d2d1_3.h)
description: Creates an ID2D1Device4 object.
helpviewer_keywords: ["CreateDevice","CreateDevice method [Direct2D]","CreateDevice method [Direct2D]","ID2D1Factory5 interface","ID2D1Factory5 interface [Direct2D]","CreateDevice method","ID2D1Factory5.CreateDevice","ID2D1Factory5::CreateDevice","d2d1_3/ID2D1Factory5::CreateDevice","direct2d.id2d1factory5_createdevice"]
old-location: direct2d\id2d1factory5_createdevice.htm
tech.root: Direct2D
ms.assetid: BE77F5AD-82B1-4DB4-8BE0-8C066EA09424
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory5 interface, ID2D1Factory5 interface [Direct2D],CreateDevice method, ID2D1Factory5.CreateDevice, ID2D1Factory5::CreateDevice, d2d1_3/ID2D1Factory5::CreateDevice, direct2d.id2d1factory5_createdevice
req.header: d2d1_3.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory5::CreateDevice
 - d2d1_3/ID2D1Factory5::CreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory5.CreateDevice
---

## -description

Creates an <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a> object.

## -parameters

### -param dxgiDevice [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>*</b>

The IDXGIDevice object used when creating the <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a>.

### -param d2dDevice4 [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a>**</b>

The requested <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a> object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1factory5">ID2D1Factory5</a>