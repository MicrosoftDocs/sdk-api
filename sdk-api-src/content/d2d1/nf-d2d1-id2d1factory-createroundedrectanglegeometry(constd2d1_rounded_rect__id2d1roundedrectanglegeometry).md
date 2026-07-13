---
UID: NF:d2d1.ID2D1Factory.CreateRoundedRectangleGeometry(constD2D1_ROUNDED_RECT&,ID2D1RoundedRectangleGeometry)
title: ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry) (d2d1.h)
description: Creates an ID2D1RoundedRectangleGeometry. (overload 2/2)
helpviewer_keywords: ["CreateRoundedRectangleGeometry","CreateRoundedRectangleGeometry method [Direct2D]","CreateRoundedRectangleGeometry method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateRoundedRectangleGeometry method","ID2D1Factory.CreateRoundedRectangleGeometry","ID2D1Factory.CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &","ID2D1RoundedRectangleGeometry)","ID2D1Factory::CreateRoundedRectangleGeometry","ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &","ID2D1RoundedRectangleGeometry)","d2d1/ID2D1Factory::CreateRoundedRectangleGeometry","direct2d.ID2D1Factory_CreateRoundedRectangleGeometry_ref_D2D1_ROUNDED_RECT_ptr_ptr_ID2D1RoundedRectangleGeometry"]
old-location: direct2d\ID2D1Factory_CreateRoundedRectangleGeometry_ref_D2D1_ROUNDED_RECT_ptr_ptr_ID2D1RoundedRectangleGeometry.htm
tech.root: Direct2D
ms.assetid: a779a6ad-2d86-416f-8f3f-1ccc90c13572
ms.date: 12/05/2018
ms.keywords: CreateRoundedRectangleGeometry, CreateRoundedRectangleGeometry method [Direct2D], CreateRoundedRectangleGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateRoundedRectangleGeometry method, ID2D1Factory.CreateRoundedRectangleGeometry, ID2D1Factory.CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry), ID2D1Factory::CreateRoundedRectangleGeometry, ID2D1Factory::CreateRoundedRectangleGeometry(const D2D1_ROUNDED_RECT &,ID2D1RoundedRectangleGeometry), d2d1/ID2D1Factory::CreateRoundedRectangleGeometry, direct2d.ID2D1Factory_CreateRoundedRectangleGeometry_ref_D2D1_ROUNDED_RECT_ptr_ptr_ID2D1RoundedRectangleGeometry
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
 - ID2D1Factory::CreateRoundedRectangleGeometry
 - d2d1/ID2D1Factory::CreateRoundedRectangleGeometry
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
 - ID2D1Factory.CreateRoundedRectangleGeometry
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>.

## -parameters

### -param roundedRectangle

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_rounded_rect">D2D1_ROUNDED_RECT</a> &</b>

The coordinates and corner radii of the rounded rectangle geometry.

### -param roundedRectangleGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rounded rectangle geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

