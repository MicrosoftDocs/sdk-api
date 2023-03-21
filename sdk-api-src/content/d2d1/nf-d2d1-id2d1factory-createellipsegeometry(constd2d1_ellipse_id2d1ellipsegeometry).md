---
UID: NF:d2d1.ID2D1Factory.CreateEllipseGeometry(constD2D1_ELLIPSE,ID2D1EllipseGeometry)
title: ID2D1Factory::CreateEllipseGeometry (d2d1.h)
description: Creates an ID2D1EllipseGeometry. (overload 1/2)
helpviewer_keywords: ["CreateEllipseGeometry","CreateEllipseGeometry methods [Direct2D]","ID2D1Factory.CreateEllipseGeometry","ID2D1Factory::CreateEllipseGeometry","d2d1/CreateEllipseGeometry","direct2d.id2d1factory_createellipsegeometry"]
old-location: direct2d\id2d1factory_createellipsegeometry.htm
tech.root: Direct2D
ms.assetid: 4c03bb0b-74fe-456a-aa26-5449d758c0ea
ms.date: 12/05/2018
ms.keywords: CreateEllipseGeometry, CreateEllipseGeometry methods [Direct2D], ID2D1Factory.CreateEllipseGeometry, ID2D1Factory::CreateEllipseGeometry, d2d1/CreateEllipseGeometry, direct2d.id2d1factory_createellipsegeometry
req.header: d2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory::CreateEllipseGeometry
 - d2d1/ID2D1Factory::CreateEllipseGeometry
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
 - ID2D1Factory::CreateEllipseGeometry
---

## -description

<span>Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>.

## -parameters

### -param ellipse

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a>*</b>

A value that describes the center point, x-radius, and y-radius of the ellipse geometry.

### -param ellipseGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>**</b>

When this method returns, contains the address of the pointer to the ellipse geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

