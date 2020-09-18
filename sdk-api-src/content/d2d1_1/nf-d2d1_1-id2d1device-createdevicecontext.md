---
UID: NF:d2d1_1.ID2D1Device.CreateDeviceContext
title: ID2D1Device::CreateDeviceContext (d2d1_1.h)
description: Creates a new device context from a Direct2D device.
helpviewer_keywords: ["CreateDeviceContext","CreateDeviceContext method [Direct2D]","CreateDeviceContext method [Direct2D]","ID2D1Device interface","ID2D1Device interface [Direct2D]","CreateDeviceContext method","ID2D1Device.CreateDeviceContext","ID2D1Device::CreateDeviceContext","d2d1_1/ID2D1Device::CreateDeviceContext","direct2d.id2d1device_createdevicecontext"]
old-location: direct2d\id2d1device_createdevicecontext.htm
tech.root: Direct2D
ms.assetid: d14255d4-ae59-42b4-ada9-bd7a3c5e8024
ms.date: 12/05/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device interface, ID2D1Device interface [Direct2D],CreateDeviceContext method, ID2D1Device.CreateDeviceContext, ID2D1Device::CreateDeviceContext, d2d1_1/ID2D1Device::CreateDeviceContext, direct2d.id2d1device_createdevicecontext
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1Device::CreateDeviceContext
 - d2d1_1/ID2D1Device::CreateDeviceContext
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
 - ID2D1Device.CreateDeviceContext
---

# ID2D1Device::CreateDeviceContext


## -description

Creates a new device context from a Direct2D device.

## -parameters

### -param options

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.

### -param deviceContext [out]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>**</b>

When this method returns, contains the address of a pointer to the new device context.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The new device context will not have a  selected target bitmap. The caller must create and select a bitmap as the target surface of the context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget">ID2D1DeviceContext::SetTarget</a>