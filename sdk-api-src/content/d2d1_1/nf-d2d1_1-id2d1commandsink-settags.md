---
UID: NF:d2d1_1.ID2D1CommandSink.SetTags
title: ID2D1CommandSink::SetTags (d2d1_1.h)
description: Sets the tags that correspond to the tags in the command sink.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetTags method","ID2D1CommandSink.SetTags","ID2D1CommandSink::SetTags","SetTags","SetTags method [Direct2D]","SetTags method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetTags","direct2d.id2d1commandsink_settags"]
old-location: direct2d\id2d1commandsink_settags.htm
tech.root: Direct2D
ms.assetid: 56898541-8c4a-4dbb-aa34-cc957b1f17ff
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetTags method, ID2D1CommandSink.SetTags, ID2D1CommandSink::SetTags, SetTags, SetTags method [Direct2D], SetTags method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetTags, direct2d.id2d1commandsink_settags
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
 - ID2D1CommandSink::SetTags
 - d2d1_1/ID2D1CommandSink::SetTags
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
 - ID2D1CommandSink.SetTags
---

# ID2D1CommandSink::SetTags


## -description

Sets the tags that correspond to the tags in the command sink.

## -parameters

### -param tag1

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

The first tag to associate with the primitive.

### -param tag2

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

The second tag to associate with the primitive.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-settags">ID2D1RenderTarget::SetTags</a>