---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.SetFillMode
title: ID2D1SimplifiedGeometrySink::SetFillMode (d2d1.h)
description: Specifies the method used to determine which points are inside the geometry described by this geometry sink and which points are outside.
helpviewer_keywords: ["ID2D1SimplifiedGeometrySink interface [Direct2D]","SetFillMode method","ID2D1SimplifiedGeometrySink.SetFillMode","ID2D1SimplifiedGeometrySink::SetFillMode","SetFillMode","SetFillMode method [Direct2D]","SetFillMode method [Direct2D]","ID2D1SimplifiedGeometrySink interface","d2d1/ID2D1SimplifiedGeometrySink::SetFillMode","direct2d.ID2D1SimplifiedGeometrySink_SetFillMode"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_SetFillMode.htm
tech.root: Direct2D
ms.assetid: f60f48bb-989e-46a5-b77f-65da0b91a599
ms.date: 12/05/2018
ms.keywords: ID2D1SimplifiedGeometrySink interface [Direct2D],SetFillMode method, ID2D1SimplifiedGeometrySink.SetFillMode, ID2D1SimplifiedGeometrySink::SetFillMode, SetFillMode, SetFillMode method [Direct2D], SetFillMode method [Direct2D],ID2D1SimplifiedGeometrySink interface, d2d1/ID2D1SimplifiedGeometrySink::SetFillMode, direct2d.ID2D1SimplifiedGeometrySink_SetFillMode
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
 - ID2D1SimplifiedGeometrySink::SetFillMode
 - d2d1/ID2D1SimplifiedGeometrySink::SetFillMode
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
 - ID2D1SimplifiedGeometrySink.SetFillMode
---

# ID2D1SimplifiedGeometrySink::SetFillMode


## -description

Specifies the method used to determine which points are inside the geometry described by this geometry sink  and which points are outside.

## -parameters

### -param fillMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a></b>

The method used to determine whether a given point is part of the geometry.

## -remarks

The fill mode defaults to D2D1_FILL_MODE_ALTERNATE. To set the fill mode, call <b>SetFillMode</b> before the first call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a>. Not doing will put the geometry sink in an error state.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>

