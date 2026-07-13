---
UID: NF:d2d1.ID2D1PathGeometry.GetFigureCount
title: ID2D1PathGeometry::GetFigureCount (d2d1.h)
description: Retrieves the number of figures in the path geometry.
helpviewer_keywords: ["GetFigureCount","GetFigureCount method [Direct2D]","GetFigureCount method [Direct2D]","ID2D1PathGeometry interface","ID2D1PathGeometry interface [Direct2D]","GetFigureCount method","ID2D1PathGeometry.GetFigureCount","ID2D1PathGeometry::GetFigureCount","d2d1/ID2D1PathGeometry::GetFigureCount","direct2d.ID2D1PathGeometry_GetFigureCount"]
old-location: direct2d\ID2D1PathGeometry_GetFigureCount.htm
tech.root: Direct2D
ms.assetid: f46d28f6-5f46-45eb-85c9-6d3b21fa2cff
ms.date: 12/05/2018
ms.keywords: GetFigureCount, GetFigureCount method [Direct2D], GetFigureCount method [Direct2D],ID2D1PathGeometry interface, ID2D1PathGeometry interface [Direct2D],GetFigureCount method, ID2D1PathGeometry.GetFigureCount, ID2D1PathGeometry::GetFigureCount, d2d1/ID2D1PathGeometry::GetFigureCount, direct2d.ID2D1PathGeometry_GetFigureCount
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
 - ID2D1PathGeometry::GetFigureCount
 - d2d1/ID2D1PathGeometry::GetFigureCount
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
 - ID2D1PathGeometry.GetFigureCount
---

# ID2D1PathGeometry::GetFigureCount


## -description

Retrieves the number of figures in the path geometry.

## -parameters

### -param count [out]

Type: <b>UINT32*</b>

A pointer that receives the number of figures in the path geometry when this method returns. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>

