---
UID: NN:d2d1effectauthor.ID2D1EffectImpl
title: ID2D1EffectImpl (d2d1effectauthor.h)
description: Allows a custom effect's interface and behavior to be specified by the effect author.
helpviewer_keywords: ["ID2D1EffectImpl","ID2D1EffectImpl interface [Direct2D]","ID2D1EffectImpl interface [Direct2D]","described","d2d1effectauthor/ID2D1EffectImpl","direct2d.id2d1effectimpl"]
old-location: direct2d\id2d1effectimpl.htm
tech.root: Direct2D
ms.assetid: 3D87A908-FC57-4AA9-A508-C402D8413363
ms.date: 12/05/2018
ms.keywords: ID2D1EffectImpl, ID2D1EffectImpl interface [Direct2D], ID2D1EffectImpl interface [Direct2D],described, d2d1effectauthor/ID2D1EffectImpl, direct2d.id2d1effectimpl
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
 - ID2D1EffectImpl
 - d2d1effectauthor/ID2D1EffectImpl
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
 - ID2D1EffectImpl
---

# ID2D1EffectImpl interface


## -description

Allows a custom effect's interface and behavior to be specified by the effect author.

## -inheritance

The <b>ID2D1EffectImpl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1EffectImpl</b> also has these types of members:

## -remarks

This interface is created by the effect author from a static factory registered through 
      the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory::RegisterEffect</a>  method.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory::RegisterEffect</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
