---
UID: NF:d2d1_1.ID2D1CommandSink.SetTextAntialiasMode
title: ID2D1CommandSink::SetTextAntialiasMode (d2d1_1.h)
description: Indicates the new default antialiasing mode for text.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetTextAntialiasMode method","ID2D1CommandSink.SetTextAntialiasMode","ID2D1CommandSink::SetTextAntialiasMode","SetTextAntialiasMode","SetTextAntialiasMode method [Direct2D]","SetTextAntialiasMode method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetTextAntialiasMode","direct2d.id2d1commandsink_settextantialiasmode"]
old-location: direct2d\id2d1commandsink_settextantialiasmode.htm
tech.root: Direct2D
ms.assetid: c6bd9c50-b0a5-4d5e-b554-1c4caa6d8e00
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetTextAntialiasMode method, ID2D1CommandSink.SetTextAntialiasMode, ID2D1CommandSink::SetTextAntialiasMode, SetTextAntialiasMode, SetTextAntialiasMode method [Direct2D], SetTextAntialiasMode method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetTextAntialiasMode, direct2d.id2d1commandsink_settextantialiasmode
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
 - ID2D1CommandSink::SetTextAntialiasMode
 - d2d1_1/ID2D1CommandSink::SetTextAntialiasMode
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
 - ID2D1CommandSink.SetTextAntialiasMode
---

# ID2D1CommandSink::SetTextAntialiasMode


## -description

Indicates the new default antialiasing mode for text.

## -parameters

### -param textAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for the text.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">ID2D1RenderTarget::SetTextAntialiasMode</a>