---
UID: NN:d2d1_1.ID2D1DeviceContext
title: ID2D1DeviceContext (d2d1_1.h)
description: Represents a set of state and command buffers that are used to render to a target.
helpviewer_keywords: ["ID2D1DeviceContext","ID2D1DeviceContext interface [Direct2D]","ID2D1DeviceContext interface [Direct2D]","described","d2d1_1/ID2D1DeviceContext","direct2d.id2d1devicecontext"]
old-location: direct2d\id2d1devicecontext.htm
tech.root: Direct2D
ms.assetid: a54dd628-c2a2-4b04-9ced-7749a395f187
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext, ID2D1DeviceContext interface [Direct2D], ID2D1DeviceContext interface [Direct2D],described, d2d1_1/ID2D1DeviceContext, direct2d.id2d1devicecontext
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext
 - d2d1_1/ID2D1DeviceContext
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
 - ID2D1DeviceContext
---

# ID2D1DeviceContext interface


## -description

Represents a set of state and command buffers that are used to render to a target.

The device context can render to a target bitmap or a command list.

## -inheritance

The <b>ID2D1DeviceContext</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. <b>ID2D1DeviceContext</b> also has these types of members:

## -remarks

 Any resource created from a device context can be shared with any other resource created from a device context when both contexts are created on the same device.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext">D2D1CreateDeviceContext</a>



<a href="/windows/desktop/Direct2D/devices-and-device-contexts">Devices and Device Contexts</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext">ID2D1Device::CreateDeviceContext</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
