---
UID: NF:dwrite.IDWriteInlineObject.GetOverhangMetrics
title: IDWriteInlineObject::GetOverhangMetrics (dwrite.h)
description: IDWriteTextLayout calls this callback function to get the visible extents (in DIPs) of the inline object. In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.
helpviewer_keywords: ["GetOverhangMetrics","GetOverhangMetrics method [Direct Write]","GetOverhangMetrics method [Direct Write]","IDWriteInlineObject interface","IDWriteInlineObject interface [Direct Write]","GetOverhangMetrics method","IDWriteInlineObject.GetOverhangMetrics","IDWriteInlineObject::GetOverhangMetrics","directwrite.idwriteinlineobject_getoverhangmetrics","dwrite/IDWriteInlineObject::GetOverhangMetrics"]
old-location: directwrite\idwriteinlineobject_getoverhangmetrics.htm
tech.root: DirectWrite
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
ms.date: 12/05/2018
ms.keywords: GetOverhangMetrics, GetOverhangMetrics method [Direct Write], GetOverhangMetrics method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetOverhangMetrics method, IDWriteInlineObject.GetOverhangMetrics, IDWriteInlineObject::GetOverhangMetrics, directwrite.idwriteinlineobject_getoverhangmetrics, dwrite/IDWriteInlineObject::GetOverhangMetrics
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteInlineObject::GetOverhangMetrics
 - dwrite/IDWriteInlineObject::GetOverhangMetrics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteInlineObject.GetOverhangMetrics
---

# IDWriteInlineObject::GetOverhangMetrics


## -description

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> calls this callback function to get the visible extents (in DIPs) of the inline object. In the case of a simple bitmap, with no padding and no overhang, all the overhangs will
    simply be zeroes.

The overhangs should be returned relative to the reported size of the object (see <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics">DWRITE_INLINE_OBJECT_METRICS</a>), and should not be baseline
    adjusted.

## -parameters

### -param overhangs [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics">DWRITE_OVERHANG_METRICS</a>*</b>

Overshoot of visible extents (in DIPs) outside the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>

