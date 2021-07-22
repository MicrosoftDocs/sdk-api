---
UID: NF:d2d1_3.ID2D1GdiMetafile1.GetDpi
title: ID2D1GdiMetafile1::GetDpi (d2d1_3.h)
description: Gets the DPI reported by the metafile.
helpviewer_keywords: ["GetDpi","GetDpi method [Direct2D]","GetDpi method [Direct2D]","ID2D1GdiMetafile1 interface","ID2D1GdiMetafile1 interface [Direct2D]","GetDpi method","ID2D1GdiMetafile1.GetDpi","ID2D1GdiMetafile1::GetDpi","d2d1_3/ID2D1GdiMetafile1::GetDpi","direct2d.id2d1gdimetafile1_getdpi"]
old-location: direct2d\id2d1gdimetafile1_getdpi.htm
tech.root: Direct2D
ms.assetid: 21238137-034c-9439-8b42-aba1be6a69af
ms.date: 12/05/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1GdiMetafile1 interface, ID2D1GdiMetafile1 interface [Direct2D],GetDpi method, ID2D1GdiMetafile1.GetDpi, ID2D1GdiMetafile1::GetDpi, d2d1_3/ID2D1GdiMetafile1::GetDpi, direct2d.id2d1gdimetafile1_getdpi
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GdiMetafile1::GetDpi
 - d2d1_3/ID2D1GdiMetafile1::GetDpi
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
 - ID2D1GdiMetafile1.GetDpi
---

# ID2D1GdiMetafile1::GetDpi


## -description

Gets the DPI reported by the metafile.

## -parameters

### -param dpiX [out]

Type: <b>FLOAT*</b>

Receives the horizontal DPI reported by the metafile.

### -param dpiY [out]

Type: <b>FLOAT*</b>

Receives the vertical DPI reported by the metafile.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile1</a>