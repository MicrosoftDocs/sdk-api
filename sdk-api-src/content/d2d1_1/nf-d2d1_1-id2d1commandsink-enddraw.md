---
UID: NF:d2d1_1.ID2D1CommandSink.EndDraw
title: ID2D1CommandSink::EndDraw (d2d1_1.h)
description: Indicates when ID2D1CommandSink processing has completed.
helpviewer_keywords: ["EndDraw","EndDraw method [Direct2D]","EndDraw method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","EndDraw method","ID2D1CommandSink.EndDraw","ID2D1CommandSink::EndDraw","d2d1_1/ID2D1CommandSink::EndDraw","direct2d.id2d1commandsink_enddraw"]
old-location: direct2d\id2d1commandsink_enddraw.htm
tech.root: Direct2D
ms.assetid: 7324d66b-b415-4e07-9fe3-d79a1c0a49b0
ms.date: 12/05/2018
ms.keywords: EndDraw, EndDraw method [Direct2D], EndDraw method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],EndDraw method, ID2D1CommandSink.EndDraw, ID2D1CommandSink::EndDraw, d2d1_1/ID2D1CommandSink::EndDraw, direct2d.id2d1commandsink_enddraw
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
 - ID2D1CommandSink::EndDraw
 - d2d1_1/ID2D1CommandSink::EndDraw
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
 - ID2D1CommandSink.EndDraw
---

# ID2D1CommandSink::EndDraw


## -description

Indicates when  <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a> processing has completed.



## -returns

Type: <b>HRESULT</b>

If the method/function succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>HRESULT</b> active at the end of the command list will be returned.

 It allows the calling function or method to indicate a failure back to the stream implementation.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a>
