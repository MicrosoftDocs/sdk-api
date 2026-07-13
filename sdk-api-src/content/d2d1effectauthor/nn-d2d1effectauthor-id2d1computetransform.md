---
UID: NN:d2d1effectauthor.ID2D1ComputeTransform
title: ID2D1ComputeTransform (d2d1effectauthor.h)
description: Defines a transform that uses a compute shader.
helpviewer_keywords: ["ID2D1ComputeTransform","ID2D1ComputeTransform interface [Direct2D]","ID2D1ComputeTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1ComputeTransform","direct2d.id2d1computetransform"]
old-location: direct2d\id2d1computetransform.htm
tech.root: Direct2D
ms.assetid: 2D7B82E1-6EB7-492A-B65C-CE5EFBFACC31
ms.date: 12/05/2018
ms.keywords: ID2D1ComputeTransform, ID2D1ComputeTransform interface [Direct2D], ID2D1ComputeTransform interface [Direct2D],described, d2d1effectauthor/ID2D1ComputeTransform, direct2d.id2d1computetransform
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
 - ID2D1ComputeTransform
 - d2d1effectauthor/ID2D1ComputeTransform
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
 - ID2D1ComputeTransform
---

# ID2D1ComputeTransform interface


## -description

Defines a transform that uses a compute shader.

## -inheritance

The <b>ID2D1ComputeTransform</b> interface inherits from <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>. <b>ID2D1ComputeTransform</b> also has these types of members:

## -remarks

The transform implements the normal Shatzis methods by  implementing <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>. In addition, the caller is passed an <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo">ID2D1ComputeInfo</a> to describe the compute pass that the transform should execute.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>
