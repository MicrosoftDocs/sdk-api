---
UID: NN:d2d1effectauthor.ID2D1EffectContext
title: ID2D1EffectContext (d2d1effectauthor.h)
description: Provides factory methods and other state management for effect and transform authors. (ID2D1EffectContext)
helpviewer_keywords: ["ID2D1EffectContext","ID2D1EffectContext interface [Direct2D]","ID2D1EffectContext interface [Direct2D]","described","d2d1effectauthor/ID2D1EffectContext","direct2d.id2d1contextinternal"]
old-location: direct2d\id2d1contextinternal.htm
tech.root: Direct2D
ms.assetid: 6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE
ms.date: 12/05/2018
ms.keywords: ID2D1EffectContext, ID2D1EffectContext interface [Direct2D], ID2D1EffectContext interface [Direct2D],described, d2d1effectauthor/ID2D1EffectContext, direct2d.id2d1contextinternal
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext
 - d2d1effectauthor/ID2D1EffectContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext
---

# ID2D1EffectContext interface


## -description

Provides factory methods and other state management for effect and transform authors.

## -inheritance

The <b>ID2D1EffectContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1EffectContext</b> also has these types of members:

## -remarks

This interface  is passed to an effect implementation through the <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1EffectImpl::Initialize</a> method. In order to prevent applications casually gaining access to this interface, and to separate reference counts between the public and private interfaces, it is not possible to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> between the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> and the <b>ID2D1EffectContext</b>.

Each call to <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize">ID2D1Effect::Initialize</a> will be provided a different <b>ID2D1EffectContext</b> interface. This interface tracks resource allocations for the effect. When the effect is released, the corresponding allocations will also be released.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory::RegisterEffect</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
