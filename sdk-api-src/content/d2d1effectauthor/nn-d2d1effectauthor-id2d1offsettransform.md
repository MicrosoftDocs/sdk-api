---
UID: NN:d2d1effectauthor.ID2D1OffsetTransform
title: ID2D1OffsetTransform (d2d1effectauthor.h)
description: Instructs the effect-rendering system to offset an input bitmap without inserting a rendering pass.
helpviewer_keywords: ["ID2D1OffsetTransform","ID2D1OffsetTransform interface [Direct2D]","ID2D1OffsetTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1OffsetTransform","direct2d.id2d1offsettransform"]
old-location: direct2d\id2d1offsettransform.htm
tech.root: Direct2D
ms.assetid: 0809C0FC-2F7B-49D8-A695-AD451C9BD17F
ms.date: 12/05/2018
ms.keywords: ID2D1OffsetTransform, ID2D1OffsetTransform interface [Direct2D], ID2D1OffsetTransform interface [Direct2D],described, d2d1effectauthor/ID2D1OffsetTransform, direct2d.id2d1offsettransform
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1OffsetTransform
 - d2d1effectauthor/ID2D1OffsetTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1OffsetTransform
---

# ID2D1OffsetTransform interface


## -description

Instructs the effect-rendering system to offset an input bitmap without inserting a rendering pass.

## -inheritance

The <b>ID2D1OffsetTransform</b> interface inherits from <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>. <b>ID2D1OffsetTransform</b> also has these types of members:

## -remarks

Because a rendering pass is not required, the interface derives from a transform node. This allows it to be inserted into a graph but does not allow an output buffer to be specified.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform">I2D1DeviceContext::CreateOffsetTransform</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>
