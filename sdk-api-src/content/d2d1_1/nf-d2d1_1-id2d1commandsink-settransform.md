---
UID: NF:d2d1_1.ID2D1CommandSink.SetTransform
title: ID2D1CommandSink::SetTransform (d2d1_1.h)
description: Sets a new transform.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetTransform method","ID2D1CommandSink.SetTransform","ID2D1CommandSink::SetTransform","SetTransform","SetTransform method [Direct2D]","SetTransform method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetTransform","direct2d.id2d1commandsink_settransform"]
old-location: direct2d\id2d1commandsink_settransform.htm
tech.root: Direct2D
ms.assetid: bc284b13-cf22-45aa-b80c-0750622f5284
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetTransform method, ID2D1CommandSink.SetTransform, ID2D1CommandSink::SetTransform, SetTransform, SetTransform method [Direct2D], SetTransform method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetTransform, direct2d.id2d1commandsink_settransform
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
 - ID2D1CommandSink::SetTransform
 - d2d1_1/ID2D1CommandSink::SetTransform
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
 - ID2D1CommandSink.SetTransform
---

# ID2D1CommandSink::SetTransform


## -description

Sets a new transform.

## -parameters

### -param transform [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to be set.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The transform will be applied to the corresponding device context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/Direct2D/id2d1rendertarget-settransform">ID2D1RenderTarget::SetTransform</a>