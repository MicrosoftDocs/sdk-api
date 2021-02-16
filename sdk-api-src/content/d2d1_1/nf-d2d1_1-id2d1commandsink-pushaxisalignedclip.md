---
UID: NF:d2d1_1.ID2D1CommandSink.PushAxisAlignedClip
title: ID2D1CommandSink::PushAxisAlignedClip (d2d1_1.h)
description: Pushes a clipping rectangle onto the clip and layer stack.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","PushAxisAlignedClip method","ID2D1CommandSink.PushAxisAlignedClip","ID2D1CommandSink::PushAxisAlignedClip","PushAxisAlignedClip","PushAxisAlignedClip method [Direct2D]","PushAxisAlignedClip method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::PushAxisAlignedClip","direct2d.id2d1commandsink_pushaxisalignedclip"]
old-location: direct2d\id2d1commandsink_pushaxisalignedclip.htm
tech.root: Direct2D
ms.assetid: 09e20780-2ebd-417e-9953-421f49dba4dd
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],PushAxisAlignedClip method, ID2D1CommandSink.PushAxisAlignedClip, ID2D1CommandSink::PushAxisAlignedClip, PushAxisAlignedClip, PushAxisAlignedClip method [Direct2D], PushAxisAlignedClip method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::PushAxisAlignedClip, direct2d.id2d1commandsink_pushaxisalignedclip
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
 - ID2D1CommandSink::PushAxisAlignedClip
 - d2d1_1/ID2D1CommandSink::PushAxisAlignedClip
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
 - ID2D1CommandSink.PushAxisAlignedClip
---

# ID2D1CommandSink::PushAxisAlignedClip


## -description

Pushes a clipping rectangle onto the clip and layer stack.

## -parameters

### -param clipRect [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rectangle that defines the clip.

### -param antialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialias mode for the clip.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

If the current world transform is not preserving the axis, <i>clipRectangle</i> is transformed and the bounds of the transformed rectangle are used instead.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)">ID2D1RenderTarget::PushAxisAlignedClip</a>