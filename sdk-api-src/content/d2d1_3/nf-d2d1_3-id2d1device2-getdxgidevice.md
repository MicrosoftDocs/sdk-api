---
UID: NF:d2d1_3.ID2D1Device2.GetDxgiDevice
title: ID2D1Device2::GetDxgiDevice (d2d1_3.h)
description: Returns the DXGI device associated with this Direct2D device.
helpviewer_keywords: ["GetDxgiDevice","GetDxgiDevice method [Direct2D]","GetDxgiDevice method [Direct2D]","ID2D1Device2 interface","ID2D1Device2 interface [Direct2D]","GetDxgiDevice method","ID2D1Device2.GetDxgiDevice","ID2D1Device2::GetDxgiDevice","d2d1_3/ID2D1Device2::GetDxgiDevice","direct2d.id2d1device2_getdxgidevice"]
old-location: direct2d\id2d1device2_getdxgidevice.htm
tech.root: Direct2D
ms.assetid: b0495244-d641-24d8-f1e2-0de1e8f84426
ms.date: 12/05/2018
ms.keywords: GetDxgiDevice, GetDxgiDevice method [Direct2D], GetDxgiDevice method [Direct2D],ID2D1Device2 interface, ID2D1Device2 interface [Direct2D],GetDxgiDevice method, ID2D1Device2.GetDxgiDevice, ID2D1Device2::GetDxgiDevice, d2d1_3/ID2D1Device2::GetDxgiDevice, direct2d.id2d1device2_getdxgidevice
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device2::GetDxgiDevice
 - d2d1_3/ID2D1Device2::GetDxgiDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Device2.GetDxgiDevice
---

# ID2D1Device2::GetDxgiDevice


## -description

Returns the DXGI device associated with this Direct2D device.

## -parameters

### -param dxgiDevice [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>**</b>

The DXGI device associated with this Direct2D device.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device2">ID2D1Device2</a>