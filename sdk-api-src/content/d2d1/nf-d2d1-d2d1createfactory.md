---
UID: NF:d2d1.D2D1CreateFactory
title: D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS*,void**)
description: D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS*,void**) creates a factory object that can be used to create Direct2D resources.
helpviewer_keywords: ["D2D1CreateFactory","D2D1CreateFactory function [Direct2D]","D2D1CreateFactory(D2D1_FACTORY_TYPE","REFIID","D2D1_FACTORY_OPTIONS*","void**)","d2d1/D2D1CreateFactory","direct2d.d2d1createfactory"]
old-location: direct2d\d2d1createfactory.htm
tech.root: Direct2D
ms.assetid: 8c0a685a-8f33-4072-a715-bb423cb44f03
ms.date: 08/10/2022
ms.keywords: D2D1CreateFactory, D2D1CreateFactory function [Direct2D], D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS*,void**), d2d1/D2D1CreateFactory, direct2d.d2d1createfactory
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - D2D1CreateFactory
 - d2d1/D2D1CreateFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - D2D1CreateFactory
---

## -description

Creates a factory object that can be used to create Direct2D resources.

## -parameters

### -param factoryType [in]

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_factory_type">D2D1_FACTORY_TYPE</a></b>

The threading model of the factory and the resources it creates.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> that is obtained by using `__uuidof(ID2D1Factory)`.

### -param pFactoryOptions [in, optional]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_factory_options">D2D1_FACTORY_OPTIONS</a>*</b>

The level of detail provided to the debugging layer.

### -param ppIFactory [out]

Type: <b>void**</b>

When this method returns, contains the address to a pointer to the new factory.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> interface provides the starting point for Direct2D. In general, an object created from a single instance of a factory object can be used with other resources created from that instance, but not with resources created by other factory instances.

## -see-also

<a href="/windows/win32/Direct2D/the-direct2d-api">Direct2D API Overview</a>

