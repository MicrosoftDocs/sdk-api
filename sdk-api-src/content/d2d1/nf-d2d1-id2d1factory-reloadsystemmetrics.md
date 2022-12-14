---
UID: NF:d2d1.ID2D1Factory.ReloadSystemMetrics
title: ID2D1Factory::ReloadSystemMetrics (d2d1.h)
description: Forces the factory to refresh any system defaults that it might have changed since factory creation.
helpviewer_keywords: ["ID2D1Factory interface [Direct2D]","ReloadSystemMetrics method","ID2D1Factory.ReloadSystemMetrics","ID2D1Factory::ReloadSystemMetrics","ReloadSystemMetrics","ReloadSystemMetrics method [Direct2D]","ReloadSystemMetrics method [Direct2D]","ID2D1Factory interface","d2d1/ID2D1Factory::ReloadSystemMetrics","direct2d.ID2D1Factory_ReloadSystemMetrics"]
old-location: direct2d\ID2D1Factory_ReloadSystemMetrics.htm
tech.root: Direct2D
ms.assetid: 32c831c4-73e1-49f8-8d58-4248ae99fe37
ms.date: 12/05/2018
ms.keywords: ID2D1Factory interface [Direct2D],ReloadSystemMetrics method, ID2D1Factory.ReloadSystemMetrics, ID2D1Factory::ReloadSystemMetrics, ReloadSystemMetrics, ReloadSystemMetrics method [Direct2D], ReloadSystemMetrics method [Direct2D],ID2D1Factory interface, d2d1/ID2D1Factory::ReloadSystemMetrics, direct2d.ID2D1Factory_ReloadSystemMetrics
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
 - ID2D1Factory::ReloadSystemMetrics
 - d2d1/ID2D1Factory::ReloadSystemMetrics
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
 - ID2D1Factory.ReloadSystemMetrics
---

## -description

Forces the factory to refresh any system defaults that it might have changed since factory creation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

To ensure that the system DPI is current, you should call **ID2D1Factory.ReloadSystemMetrics** before calling the [GetDesktopDpi](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.

## -see-also

* [ID2D1Factory](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
