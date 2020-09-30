---
UID: NF:d2d1_1.ID2D1CommandSink.SetAntialiasMode
title: ID2D1CommandSink::SetAntialiasMode (d2d1_1.h)
description: Sets the antialiasing mode that will be used to render any subsequent geometry.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetAntialiasMode method","ID2D1CommandSink.SetAntialiasMode","ID2D1CommandSink::SetAntialiasMode","SetAntialiasMode","SetAntialiasMode method [Direct2D]","SetAntialiasMode method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetAntialiasMode","direct2d.id2d1commandsink_setantialiasmode"]
old-location: direct2d\id2d1commandsink_setantialiasmode.htm
tech.root: Direct2D
ms.assetid: 335cb9e7-56da-4971-b6d1-94292a6a771a
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetAntialiasMode method, ID2D1CommandSink.SetAntialiasMode, ID2D1CommandSink::SetAntialiasMode, SetAntialiasMode, SetAntialiasMode method [Direct2D], SetAntialiasMode method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetAntialiasMode, direct2d.id2d1commandsink_setantialiasmode
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
 - ID2D1CommandSink::SetAntialiasMode
 - d2d1_1/ID2D1CommandSink::SetAntialiasMode
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
 - ID2D1CommandSink.SetAntialiasMode
---

# ID2D1CommandSink::SetAntialiasMode


## -description

Sets the antialiasing mode that will be used to render any subsequent geometry.

## -parameters

### -param antialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode selected for the command list.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode">ID2D1RenderTarget::SetAntialiasMode</a>