---
UID: NF:d2d1_3.ID2D1GdiMetafile1.GetSourceBounds
title: ID2D1GdiMetafile1::GetSourceBounds (d2d1_3.h)
description: Gets the bounds of the metafile in source space in DIPs. This corresponds to the frame rect in an EMF/EMF+.
helpviewer_keywords: ["GetSourceBounds","GetSourceBounds method [Direct2D]","GetSourceBounds method [Direct2D]","ID2D1GdiMetafile1 interface","ID2D1GdiMetafile1 interface [Direct2D]","GetSourceBounds method","ID2D1GdiMetafile1.GetSourceBounds","ID2D1GdiMetafile1::GetSourceBounds","d2d1_3/ID2D1GdiMetafile1::GetSourceBounds","direct2d.id2d1gdimetafile1_getsourcebounds"]
old-location: direct2d\id2d1gdimetafile1_getsourcebounds.htm
tech.root: Direct2D
ms.assetid: 7e7502ee-678e-ce26-cc0b-266faa1c320b
ms.date: 12/05/2018
ms.keywords: GetSourceBounds, GetSourceBounds method [Direct2D], GetSourceBounds method [Direct2D],ID2D1GdiMetafile1 interface, ID2D1GdiMetafile1 interface [Direct2D],GetSourceBounds method, ID2D1GdiMetafile1.GetSourceBounds, ID2D1GdiMetafile1::GetSourceBounds, d2d1_3/ID2D1GdiMetafile1::GetSourceBounds, direct2d.id2d1gdimetafile1_getsourcebounds
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
 - ID2D1GdiMetafile1::GetSourceBounds
 - d2d1_3/ID2D1GdiMetafile1::GetSourceBounds
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
 - ID2D1GdiMetafile1.GetSourceBounds
---

# ID2D1GdiMetafile1::GetSourceBounds


## -description

Gets the bounds of the metafile in source space in DIPs. This corresponds      
    to the frame rect in an EMF/EMF+.

## -parameters

### -param bounds [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The bounds, in DIPs, of the metafile.

## -returns

Type: <b>HRESULT</b>

S_OK if successful, otherwise a failure HRESULT.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>



<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gdimetafile1">ID2D1GdiMetafile1</a>



<a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">[MS-EMFPLUS]: Enhanced Metafile Format Plus Extensions</a>



<a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">[MS-EMF]: Enhanced Metafile Format</a>