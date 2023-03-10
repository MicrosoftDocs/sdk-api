---
UID: NF:d2d1.ID2D1Factory.CreateEllipseGeometry(constD2D1_ELLIPSE&,ID2D1EllipseGeometry)
title: ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE &,ID2D1EllipseGeometry) (d2d1.h)
description: Creates an ID2D1EllipseGeometry. (overload 2/2)
helpviewer_keywords: ["CreateEllipseGeometry","CreateEllipseGeometry method [Direct2D]","CreateEllipseGeometry method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateEllipseGeometry method","ID2D1Factory.CreateEllipseGeometry","ID2D1Factory.CreateEllipseGeometry(const D2D1_ELLIPSE &","ID2D1EllipseGeometry)","ID2D1Factory::CreateEllipseGeometry","ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE &","ID2D1EllipseGeometry)","d2d1/ID2D1Factory::CreateEllipseGeometry","direct2d.ID2D1Factory_CreateEllipseGeometry_ref_D2D1_ELLIPSE_ptr_ptr_ID2D1EllipseGeometry"]
old-location: direct2d\ID2D1Factory_CreateEllipseGeometry_ref_D2D1_ELLIPSE_ptr_ptr_ID2D1EllipseGeometry.htm
tech.root: Direct2D
ms.assetid: 0abbb99e-a253-44f3-90bf-0ac341e7c83d
ms.date: 12/05/2018
ms.keywords: CreateEllipseGeometry, CreateEllipseGeometry method [Direct2D], CreateEllipseGeometry method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateEllipseGeometry method, ID2D1Factory.CreateEllipseGeometry, ID2D1Factory.CreateEllipseGeometry(const D2D1_ELLIPSE &,ID2D1EllipseGeometry), ID2D1Factory::CreateEllipseGeometry, ID2D1Factory::CreateEllipseGeometry(const D2D1_ELLIPSE &,ID2D1EllipseGeometry), d2d1/ID2D1Factory::CreateEllipseGeometry, direct2d.ID2D1Factory_CreateEllipseGeometry_ref_D2D1_ELLIPSE_ptr_ptr_ID2D1EllipseGeometry
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
 - ID2D1Factory::CreateEllipseGeometry
 - d2d1/ID2D1Factory::CreateEllipseGeometry
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
 - ID2D1Factory.CreateEllipseGeometry
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>.

## -parameters

### -param ellipse

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_ellipse">D2D1_ELLIPSE</a> &</b>

A value that describes the center point, x-radius, and y-radius of the ellipse geometry.

### -param ellipseGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>**</b>

When this method returns, contains the address of the pointer to the ellipse geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

