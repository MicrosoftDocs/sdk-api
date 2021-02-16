---
UID: NF:d2d1svg.ID2D1SvgPaint.GetId
title: ID2D1SvgPaint::GetId (d2d1svg.h)
description: Gets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.
helpviewer_keywords: ["GetId","GetId method [Direct2D]","GetId method [Direct2D]","ID2D1SvgPaint interface","ID2D1SvgPaint interface [Direct2D]","GetId method","ID2D1SvgPaint.GetId","ID2D1SvgPaint::GetId","d2d1svg/ID2D1SvgPaint::GetId","direct2d.id2d1svgpaint_getid"]
old-location: direct2d\id2d1svgpaint_getid.htm
tech.root: Direct2D
ms.assetid: 50701C5C-03F8-4DCD-A29A-2DF57846ED78
ms.date: 12/05/2018
ms.keywords: GetId, GetId method [Direct2D], GetId method [Direct2D],ID2D1SvgPaint interface, ID2D1SvgPaint interface [Direct2D],GetId method, ID2D1SvgPaint.GetId, ID2D1SvgPaint::GetId, d2d1svg/ID2D1SvgPaint::GetId, direct2d.id2d1svgpaint_getid
req.header: d2d1svg.h
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgPaint::GetId
 - d2d1svg/ID2D1SvgPaint::GetId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPaint.GetId
---

# ID2D1SvgPaint::GetId


## -description

Gets the element id which acts as the paint server. This id is used if the paint type is D2D1_SVG_PAINT_TYPE_URI.

## -parameters

### -param id [out]

Type: <b>PWSTR</b>

The element id which acts as the paint server.

### -param idCount

Type: <b>UINT32</b>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpaint">ID2D1SvgPaint</a>