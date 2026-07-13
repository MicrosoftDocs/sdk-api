---
UID: NF:d2d1_3.ID2D1Ink.AddSegments
title: ID2D1Ink::AddSegments (d2d1_3.h)
description: Adds the given segments to the end of this ink object.
helpviewer_keywords: ["AddSegments","AddSegments method [Direct2D]","AddSegments method [Direct2D]","ID2D1Ink interface","ID2D1Ink interface [Direct2D]","AddSegments method","ID2D1Ink.AddSegments","ID2D1Ink::AddSegments","d2d1_3/ID2D1Ink::AddSegments","direct2d.id2d1ink_addsegments"]
old-location: direct2d\id2d1ink_addsegments.htm
tech.root: Direct2D
ms.assetid: 0AB546AC-F7AB-4C48-AA10-3DD2FF11B853
ms.date: 12/05/2018
ms.keywords: AddSegments, AddSegments method [Direct2D], AddSegments method [Direct2D],ID2D1Ink interface, ID2D1Ink interface [Direct2D],AddSegments method, ID2D1Ink.AddSegments, ID2D1Ink::AddSegments, d2d1_3/ID2D1Ink::AddSegments, direct2d.id2d1ink_addsegments
req.header: d2d1_3.h
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Ink::AddSegments
 - d2d1_3/ID2D1Ink::AddSegments
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Ink.AddSegments
---

# ID2D1Ink::AddSegments


## -description

Adds the given segments to the end of this ink object.

## -parameters

### -param segments [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a>*</b>

A pointer to an array of segments to be added to this ink object.

### -param segmentsCount

Type: <b>UINT32</b>

The number of segments to be added to this ink object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a>