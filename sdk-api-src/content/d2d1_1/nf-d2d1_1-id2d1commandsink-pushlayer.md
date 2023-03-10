---
UID: NF:d2d1_1.ID2D1CommandSink.PushLayer
title: ID2D1CommandSink::PushLayer (d2d1_1.h)
description: Pushes a layer onto the clip and layer stack.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","PushLayer method","ID2D1CommandSink.PushLayer","ID2D1CommandSink::PushLayer","PushLayer","PushLayer method [Direct2D]","PushLayer method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::PushLayer","direct2d.id2d1commandsink_pushlayer"]
old-location: direct2d\id2d1commandsink_pushlayer.htm
tech.root: Direct2D
ms.assetid: 071d7d7a-12d7-4611-812c-103e2b9a5e56
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],PushLayer method, ID2D1CommandSink.PushLayer, ID2D1CommandSink::PushLayer, PushLayer, PushLayer method [Direct2D], PushLayer method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::PushLayer, direct2d.id2d1commandsink_pushlayer
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
 - ID2D1CommandSink::PushLayer
 - d2d1_1/ID2D1CommandSink::PushLayer
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
 - ID2D1CommandSink.PushLayer
---

# ID2D1CommandSink::PushLayer


## -description

Pushes a layer onto the clip and layer stack.

## -parameters

### -param layerParameters1 [in]

Type: <b>const <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters">D2D1_LAYER_PARAMETERS1</a>*</b>

The parameters that define the layer.

### -param layer [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1layer">ID2D1Layer</a>*</b>

The layer resource that receives subsequent drawing operations.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)">ID2D1RenderTarget::PushAxisAlignedClip</a>