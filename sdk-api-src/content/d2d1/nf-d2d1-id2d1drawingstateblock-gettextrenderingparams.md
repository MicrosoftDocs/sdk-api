---
UID: NF:d2d1.ID2D1DrawingStateBlock.GetTextRenderingParams
title: ID2D1DrawingStateBlock::GetTextRenderingParams (d2d1.h)
description: Retrieves the text-rendering configuration of the drawing state.
helpviewer_keywords: ["GetTextRenderingParams","GetTextRenderingParams method [Direct2D]","GetTextRenderingParams method [Direct2D]","ID2D1DrawingStateBlock interface","ID2D1DrawingStateBlock interface [Direct2D]","GetTextRenderingParams method","ID2D1DrawingStateBlock.GetTextRenderingParams","ID2D1DrawingStateBlock::GetTextRenderingParams","d2d1/ID2D1DrawingStateBlock::GetTextRenderingParams","direct2d.ID2D1DrawingStateBlock_GetTextRenderingParams"]
old-location: direct2d\ID2D1DrawingStateBlock_GetTextRenderingParams.htm
tech.root: Direct2D
ms.assetid: 86822497-e256-445b-8da9-9ead229f89ee
ms.date: 12/05/2018
ms.keywords: GetTextRenderingParams, GetTextRenderingParams method [Direct2D], GetTextRenderingParams method [Direct2D],ID2D1DrawingStateBlock interface, ID2D1DrawingStateBlock interface [Direct2D],GetTextRenderingParams method, ID2D1DrawingStateBlock.GetTextRenderingParams, ID2D1DrawingStateBlock::GetTextRenderingParams, d2d1/ID2D1DrawingStateBlock::GetTextRenderingParams, direct2d.ID2D1DrawingStateBlock_GetTextRenderingParams
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
 - ID2D1DrawingStateBlock::GetTextRenderingParams
 - d2d1/ID2D1DrawingStateBlock::GetTextRenderingParams
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
 - ID2D1DrawingStateBlock.GetTextRenderingParams
---

# ID2D1DrawingStateBlock::GetTextRenderingParams


## -description

Retrieves the text-rendering configuration of the drawing state.

## -parameters

### -param textRenderingParams [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>**</b>

When this method returns, contains the address of a pointer to an <a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a> object that describes the text-rendering configuration of the drawing state.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>

