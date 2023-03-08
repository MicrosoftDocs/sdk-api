---
UID: NF:d2d1.ID2D1Factory.CreateRectangleGeometry(constD2D1_RECT_F&,ID2D1RectangleGeometry)
title: ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F &,ID2D1RectangleGeometry) (d2d1.h)
description: Creates an ID2D1RectangleGeometry. (overload 2/2)
helpviewer_keywords: ["CreateRectangleGeometry","CreateRectangleGeometry method [Direct2D]","CreateRectangleGeometry method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateRectangleGeometry method","ID2D1Factory.CreateRectangleGeometry","ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F &","ID2D1RectangleGeometry)","ID2D1Factory::CreateRectangleGeometry","ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F &","ID2D1RectangleGeometry)","d2d1/ID2D1Factory::CreateRectangleGeometry","direct2d.ID2D1Factory_CreateRectangleGeometry_ref_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry"]
old-location: direct2d\ID2D1Factory_CreateRectangleGeometry_ref_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry.htm
tech.root: Direct2D
ms.assetid: 536bc4c6-9347-4b7f-ab35-163636d327b6
ms.date: 12/05/2018
ms.keywords: CreateRectangleGeometry, CreateRectangleGeometry method [Direct2D], CreateRectangleGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateRectangleGeometry method, ID2D1Factory.CreateRectangleGeometry, ID2D1Factory.CreateRectangleGeometry(const D2D1_RECT_F &,ID2D1RectangleGeometry), ID2D1Factory::CreateRectangleGeometry, ID2D1Factory::CreateRectangleGeometry(const D2D1_RECT_F &,ID2D1RectangleGeometry), d2d1/ID2D1Factory::CreateRectangleGeometry, direct2d.ID2D1Factory_CreateRectangleGeometry_ref_D2D_RECT_F_ptr_ptr_ID2D1RectangleGeometry
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
 - ID2D1Factory::CreateRectangleGeometry
 - d2d1/ID2D1Factory::CreateRectangleGeometry
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
 - ID2D1Factory.CreateRectangleGeometry
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>.

## -parameters

### -param rectangle

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a> &</b>

The coordinates of the rectangle geometry.

### -param rectangleGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rectangle geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

