---
UID: NF:d2d1_3.ID2D1Device5.CreateDeviceContext
title: ID2D1Device5::CreateDeviceContext (d2d1_3.h)
description: Creates a new device context with no initially assigned target. (ID2D1Device5.CreateDeviceContext)
helpviewer_keywords: ["CreateDeviceContext","CreateDeviceContext method [Direct2D]","CreateDeviceContext method [Direct2D]","ID2D1Device5 interface","ID2D1Device5 interface [Direct2D]","CreateDeviceContext method","ID2D1Device5.CreateDeviceContext","ID2D1Device5::CreateDeviceContext","d2d1_3/ID2D1Device5::CreateDeviceContext","direct2d.id2d1device5_createdevicecontext"]
old-location: direct2d\id2d1device5_createdevicecontext.htm
tech.root: Direct2D
ms.assetid: C1C189AC-4ABD-41F8-9696-D4D76602BE61
ms.date: 12/05/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device5 interface, ID2D1Device5 interface [Direct2D],CreateDeviceContext method, ID2D1Device5.CreateDeviceContext, ID2D1Device5::CreateDeviceContext, d2d1_3/ID2D1Device5::CreateDeviceContext, direct2d.id2d1device5_createdevicecontext
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
 - ID2D1Device5::CreateDeviceContext
 - d2d1_3/ID2D1Device5::CreateDeviceContext
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
 - ID2D1Device5.CreateDeviceContext
---

# ID2D1Device5::CreateDeviceContext


## -description

Creates a new device context with no initially assigned target.

## -parameters

### -param options

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

Options for creating the device context.

### -param deviceContext5 [out]

Type: <b>ID2D1DeviceContext5**</b>

The created device context.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device5">ID2D1Device5</a>
