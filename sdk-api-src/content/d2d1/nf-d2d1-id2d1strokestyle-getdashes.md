---
UID: NF:d2d1.ID2D1StrokeStyle.GetDashes
title: ID2D1StrokeStyle::GetDashes (d2d1.h)
description: Copies the dash pattern to the specified array.
helpviewer_keywords: ["GetDashes","GetDashes method [Direct2D]","GetDashes method [Direct2D]","ID2D1StrokeStyle interface","ID2D1StrokeStyle interface [Direct2D]","GetDashes method","ID2D1StrokeStyle.GetDashes","ID2D1StrokeStyle::GetDashes","d2d1/ID2D1StrokeStyle::GetDashes","direct2d.ID2D1StrokeStyle_GetDashes"]
old-location: direct2d\ID2D1StrokeStyle_GetDashes.htm
tech.root: Direct2D
ms.assetid: b5add3b9-e052-4727-b14f-543fa452ad6d
ms.date: 12/05/2018
ms.keywords: GetDashes, GetDashes method [Direct2D], GetDashes method [Direct2D],ID2D1StrokeStyle interface, ID2D1StrokeStyle interface [Direct2D],GetDashes method, ID2D1StrokeStyle.GetDashes, ID2D1StrokeStyle::GetDashes, d2d1/ID2D1StrokeStyle::GetDashes, direct2d.ID2D1StrokeStyle_GetDashes
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
 - ID2D1StrokeStyle::GetDashes
 - d2d1/ID2D1StrokeStyle::GetDashes
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
 - ID2D1StrokeStyle.GetDashes
---

# ID2D1StrokeStyle::GetDashes


## -description

Copies the dash pattern to the specified array.

## -parameters

### -param dashes [out]

Type: <b>FLOAT*</b>

A pointer to an array that will receive the dash pattern. The array must be able to contain at least as many elements as specified by <i>dashesCount</i>. You must allocate storage for this array.

### -param dashesCount

Type: <b>UINT</b>

The number of dashes to copy. If this value is less than the number of dashes in the stroke style's dashes array, the returned dashes are truncated to <i>dashesCount</i>. If this value is greater than the number of dashes in the stroke style's dashes array, the extra dashes are set to 0.0f. To obtain the actual number of dashes in the stroke style's dashes array, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1strokestyle-getdashescount">GetDashesCount</a> method.

## -remarks

The dashes are specified in units that are a multiple of the stroke width, with subsequent members of the array indicating the dashes and gaps between dashes: the first entry indicates a filled dash, the second a gap, and so on.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>

