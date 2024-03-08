---
UID: NF:d2d1.ID2D1Factory.CreateRoundedRectangleGeometry(constD2D1_ROUNDED_RECT,ID2D1RoundedRectangleGeometry)
title: ID2D1Factory::CreateRoundedRectangleGeometry (d2d1.h)
description: Creates an ID2D1RoundedRectangleGeometry. (overload 1/2)
helpviewer_keywords: ["CreateRoundedRectangleGeometry","CreateRoundedRectangleGeometry methods [Direct2D]","ID2D1Factory.CreateRoundedRectangleGeometry","ID2D1Factory::CreateRoundedRectangleGeometry","d2d1/CreateRoundedRectangleGeometry","direct2d.id2d1factory_createroundedrectanglegeometry"]
old-location: direct2d\id2d1factory_createroundedrectanglegeometry.htm
tech.root: Direct2D
ms.assetid: b0f7ccb0-5733-4f96-a532-8f665fbc257e
ms.date: 12/05/2018
ms.keywords: CreateRoundedRectangleGeometry, CreateRoundedRectangleGeometry methods [Direct2D], ID2D1Factory.CreateRoundedRectangleGeometry, ID2D1Factory::CreateRoundedRectangleGeometry, d2d1/CreateRoundedRectangleGeometry, direct2d.id2d1factory_createroundedrectanglegeometry
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
 - ID2D1Factory::CreateRoundedRectangleGeometry
 - d2d1/ID2D1Factory::CreateRoundedRectangleGeometry
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
 - ID2D1Factory::CreateRoundedRectangleGeometry
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>.

## -parameters

### -param roundedRectangle

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_rounded_rect">D2D1_ROUNDED_RECT</a>*</b>

The coordinates and corner radii of the rounded rectangle geometry.

### -param roundedRectangleGeometry

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>**</b>

When this method returns, contains the address of the pointer to the rounded rectangle geometry created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

