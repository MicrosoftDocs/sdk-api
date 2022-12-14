---
UID: NF:d2d1_1.ID2D1CommandSink.Clear
title: ID2D1CommandSink::Clear (d2d1_1.h)
description: Clears the drawing area to the specified color. (ID2D1CommandSink.Clear)
helpviewer_keywords: ["Clear","Clear method [Direct2D]","Clear method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","Clear method","ID2D1CommandSink.Clear","ID2D1CommandSink::Clear","d2d1_1/ID2D1CommandSink::Clear","direct2d.id2d1commandsink_clear"]
old-location: direct2d\id2d1commandsink_clear.htm
tech.root: Direct2D
ms.assetid: d91bb6b2-ecc8-4c16-95fc-c0cb7bbe80e3
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Direct2D], Clear method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],Clear method, ID2D1CommandSink.Clear, ID2D1CommandSink::Clear, d2d1_1/ID2D1CommandSink::Clear, direct2d.id2d1commandsink_clear
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
 - ID2D1CommandSink::Clear
 - d2d1_1/ID2D1CommandSink::Clear
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
 - ID2D1CommandSink.Clear
---

# ID2D1CommandSink::Clear


## -description

Clears the drawing area to the specified color.

## -parameters

### -param color [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a>*</b>

The color to which the command sink should be cleared.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The clear color is restricted by the currently selected clip and layer bounds.

If no color is specified, the color should be interpreted by context. Examples include but are not limited to:

<ul>
<li>Transparent black for a premultiplied bitmap target.</li>
<li>Opaque black for an ignore bitmap target.</li>
<li>Containing no content (or white) for a printer page.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/Direct2D/id2d1rendertarget-clear">ID2D1RenderTarget::Clear</a>
