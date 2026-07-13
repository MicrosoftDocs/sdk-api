---
UID: NN:d2d1effectauthor.ID2D1BlendTransform
title: ID2D1BlendTransform (d2d1effectauthor.h)
description: Provides methods to allow a blend operation to be inserted into a transform graph.
helpviewer_keywords: ["ID2D1BlendTransform","ID2D1BlendTransform interface [Direct2D]","ID2D1BlendTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1BlendTransform","direct2d.id2d1blendtransform"]
old-location: direct2d\id2d1blendtransform.htm
tech.root: Direct2D
ms.assetid: 0DC46758-6005-4A33-9539-9C95CF8CFB6A
ms.date: 12/05/2018
ms.keywords: ID2D1BlendTransform, ID2D1BlendTransform interface [Direct2D], ID2D1BlendTransform interface [Direct2D],described, d2d1effectauthor/ID2D1BlendTransform, direct2d.id2d1blendtransform
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
 - ID2D1BlendTransform
 - d2d1effectauthor/ID2D1BlendTransform
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
 - ID2D1BlendTransform
---

# ID2D1BlendTransform interface


## -description

Provides methods to allow a blend operation to be inserted into a transform graph.

The image output of the blend transform is the same as rendering an image effect graph with these steps:
<ul>
<li>Copy the first input to the destination image.</li>
<li>Render the next input on top using the blend description.</li>
<li>Continue for each additional input.</li>
</ul>

## -inheritance

The <b>ID2D1BlendTransform</b> interface inherits from <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1concretetransform">ID2D1ConcreteTransform</a>. <b>ID2D1BlendTransform</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1concretetransform">ID2D1ConcreteTransform</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>
