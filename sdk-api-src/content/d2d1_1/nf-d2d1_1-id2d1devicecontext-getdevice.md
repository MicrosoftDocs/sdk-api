---
UID: NF:d2d1_1.ID2D1DeviceContext.GetDevice
title: ID2D1DeviceContext::GetDevice (d2d1_1.h)
description: Gets the device associated with a device context.
helpviewer_keywords: ["GetDevice","GetDevice method [Direct2D]","GetDevice method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetDevice method","ID2D1DeviceContext.GetDevice","ID2D1DeviceContext::GetDevice","d2d1_1/ID2D1DeviceContext::GetDevice","direct2d.id2d1devicecontext_getdevice"]
old-location: direct2d\id2d1devicecontext_getdevice.htm
tech.root: Direct2D
ms.assetid: 8c8664cb-d6be-41e0-8415-d60dcd46132a
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Direct2D], GetDevice method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetDevice method, ID2D1DeviceContext.GetDevice, ID2D1DeviceContext::GetDevice, d2d1_1/ID2D1DeviceContext::GetDevice, direct2d.id2d1devicecontext_getdevice
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
 - ID2D1DeviceContext::GetDevice
 - d2d1_1/ID2D1DeviceContext::GetDevice
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
 - ID2D1DeviceContext.GetDevice
---

# ID2D1DeviceContext::GetDevice


## -description

Gets the device associated with a device context.

## -parameters

### -param device [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>**</b>

When this method returns, contains the address of a pointer to a Direct2D device associated with this device context.

## -remarks

The application can retrieve the device even if it is created from an earlier render target code-path. The application must use an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> interface and then call <b>GetDevice</b>. Some functionality for controlling all of the resources for a set of device contexts is maintained only on an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> object.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>