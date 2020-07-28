---
UID: NF:d2d1.ID2D1Factory.CreateRectangleGeometry(constD2D1_RECT_F,ID2D1RectangleGeometry)
title: ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry) (d2d1.h)
description: Creates an ID2D1RectangleGeometry.
helpviewer_keywords: ["CreateRectangleGeometry","CreateRectangleGeometry method [Direct2D]","CreateRectangleGeometry method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateRectangleGeometry method","ID2D1Factory.CreateRectangleGeometry","ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F","ID2D1RectangleGeometry)","ID2D1Factory::CreateRectangleGeometry","ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F","ID2D1RectangleGeometry)","d2d1/ID2D1Factory::CreateRectangleGeometry","direct2d.ID2D1Factory_CreateRectangleGeometry_ptr_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry"]
old-location: direct2d\ID2D1Factory_CreateRectangleGeometry_ptr_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry.htm
tech.root: Direct2D
ms.assetid: 3d9a1e40-1432-4800-8d15-e2b8bda8f04f
ms.date: 12/05/2018
ms.keywords: CreateRectangleGeometry, CreateRectangleGeometry method [Direct2D], CreateRectangleGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateRectangleGeometry method, ID2D1Factory.CreateRectangleGeometry, ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry), ID2D1Factory::CreateRectangleGeometry, ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F,ID2D1RectangleGeometry), d2d1/ID2D1Factory::CreateRectangleGeometry, direct2d.ID2D1Factory_CreateRectangleGeometry_ptr_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry
f1_keywords:
- d2d1/ID2D1Factory.CreateRectangleGeometry
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Factory.CreateRectangleGeometry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>. 

## -parameters

### -param rectangle

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The coordinates of the rectangle geometry. 

### -param rectangleGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rectangle geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
