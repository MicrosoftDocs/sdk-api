---
UID: NF:dwrite.IDWriteInlineObject.GetMetrics
title: IDWriteInlineObject::GetMetrics (dwrite.h)
description: IDWriteTextLayout calls this callback function to get the measurement of the inline object.
helpviewer_keywords: ["GetMetrics","GetMetrics method [Direct Write]","GetMetrics method [Direct Write]","IDWriteInlineObject interface","IDWriteInlineObject interface [Direct Write]","GetMetrics method","IDWriteInlineObject.GetMetrics","IDWriteInlineObject::GetMetrics","directwrite.IDWriteInlineObject_GetMetrics","dwrite/IDWriteInlineObject::GetMetrics"]
old-location: directwrite\IDWriteInlineObject_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 809a4e29-0423-40b2-9d40-105d30574fa1
ms.date: 12/05/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetMetrics method, IDWriteInlineObject.GetMetrics, IDWriteInlineObject::GetMetrics, directwrite.IDWriteInlineObject_GetMetrics, dwrite/IDWriteInlineObject::GetMetrics
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteInlineObject::GetMetrics
 - dwrite/IDWriteInlineObject::GetMetrics
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
 - IDWriteInlineObject.GetMetrics
---

# IDWriteInlineObject::GetMetrics


## -description

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> calls this callback function to get the measurement of the inline object.

## -parameters

### -param metrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics">DWRITE_INLINE_OBJECT_METRICS</a>*</b>

When this method returns, contains a structure describing the geometric measurement of an
application-defined inline object.  These metrics are in relation to the baseline of the adjacent text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>

