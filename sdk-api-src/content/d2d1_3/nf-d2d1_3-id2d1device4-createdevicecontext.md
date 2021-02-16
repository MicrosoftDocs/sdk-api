---
UID: NF:d2d1_3.ID2D1Device4.CreateDeviceContext
title: ID2D1Device4::CreateDeviceContext (d2d1_3.h)
description: Creates a new ID2D1DeviceContext4 from this Direct2D device.
helpviewer_keywords: ["CreateDeviceContext","CreateDeviceContext method [Direct2D]","CreateDeviceContext method [Direct2D]","ID2D1Device4 interface","ID2D1Device4 interface [Direct2D]","CreateDeviceContext method","ID2D1Device4.CreateDeviceContext","ID2D1Device4::CreateDeviceContext","d2d1_3/ID2D1Device4::CreateDeviceContext","direct2d.id2d1device4_createdevicecontext"]
old-location: direct2d\id2d1device4_createdevicecontext.htm
tech.root: Direct2D
ms.assetid: 06F097C4-E417-48EA-A480-62E96C4A1CE6
ms.date: 12/05/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device4 interface, ID2D1Device4 interface [Direct2D],CreateDeviceContext method, ID2D1Device4.CreateDeviceContext, ID2D1Device4::CreateDeviceContext, d2d1_3/ID2D1Device4::CreateDeviceContext, direct2d.id2d1device4_createdevicecontext
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
 - ID2D1Device4::CreateDeviceContext
 - d2d1_3/ID2D1Device4::CreateDeviceContext
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
 - ID2D1Device4.CreateDeviceContext
---

# ID2D1Device4::CreateDeviceContext


## -description

Creates a new <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a> from this Direct2D device.

## -parameters

### -param options

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.

### -param deviceContext4 [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>**</b>

When this method returns, contains a pointer to the new device context.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a>