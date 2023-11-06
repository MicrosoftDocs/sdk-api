---
UID: NF:d2d1_3.ID2D1Factory4.CreateDevice
title: ID2D1Factory4::CreateDevice (d2d1_3.h)
description: Creates an ID2D1Device3 object.
helpviewer_keywords: ["CreateDevice","CreateDevice method [Direct2D]","CreateDevice method [Direct2D]","ID2D1Factory4 interface","ID2D1Factory4 interface [Direct2D]","CreateDevice method","ID2D1Factory4.CreateDevice","ID2D1Factory4::CreateDevice","d2d1_3/ID2D1Factory4::CreateDevice","direct2d.id2d1factory4_createdevice"]
old-location: direct2d\id2d1factory4_createdevice.htm
tech.root: Direct2D
ms.assetid: CF34DB7E-39CC-4044-9DF4-838EC19C1B04
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory4 interface, ID2D1Factory4 interface [Direct2D],CreateDevice method, ID2D1Factory4.CreateDevice, ID2D1Factory4::CreateDevice, d2d1_3/ID2D1Factory4::CreateDevice, direct2d.id2d1factory4_createdevice
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory4::CreateDevice
 - d2d1_3/ID2D1Factory4::CreateDevice
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
 - ID2D1Factory4.CreateDevice
---

## -description

Creates an <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a> object.

## -parameters

### -param dxgiDevice [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>*</b>

The IDXGIDevice object used when creating the <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a>.

### -param d2dDevice3 [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a>**</b>

The requested <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device3">ID2D1Device3</a> object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1factory4">ID2D1Factory4</a>