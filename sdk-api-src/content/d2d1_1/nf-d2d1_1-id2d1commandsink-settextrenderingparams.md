---
UID: NF:d2d1_1.ID2D1CommandSink.SetTextRenderingParams
title: ID2D1CommandSink::SetTextRenderingParams (d2d1_1.h)
description: Indicates more detailed text rendering parameters.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetTextRenderingParams method","ID2D1CommandSink.SetTextRenderingParams","ID2D1CommandSink::SetTextRenderingParams","SetTextRenderingParams","SetTextRenderingParams method [Direct2D]","SetTextRenderingParams method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetTextRenderingParams","direct2d.id2d1commandsink_settextrendeingparams"]
old-location: direct2d\id2d1commandsink_settextrendeingparams.htm
tech.root: Direct2D
ms.assetid: e847f2e3-6d2d-45e6-b1ef-bf393ed53e2b
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetTextRenderingParams method, ID2D1CommandSink.SetTextRenderingParams, ID2D1CommandSink::SetTextRenderingParams, SetTextRenderingParams, SetTextRenderingParams method [Direct2D], SetTextRenderingParams method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetTextRenderingParams, direct2d.id2d1commandsink_settextrendeingparams
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1CommandSink::SetTextRenderingParams
 - d2d1_1/ID2D1CommandSink::SetTextRenderingParams
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
 - ID2D1CommandSink.SetTextRenderingParams
---

# ID2D1CommandSink::SetTextRenderingParams


## -description

Indicates more detailed text rendering parameters.

## -parameters

### -param textRenderingParams [in]

Type: <b><a href="/windows/desktop/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>*</b>

The parameters to use for text rendering.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-settags">ID2D1RenderTarget::SetTags</a>