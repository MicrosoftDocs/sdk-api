---
UID: NN:d2d1.ID2D1RenderTarget
title: ID2D1RenderTarget (d2d1.h)
description: Represents an object that can receive drawing commands. Interfaces that inherit from ID2D1RenderTarget render the drawing commands they receive in different ways.
helpviewer_keywords: ["ID2D1RenderTarget","ID2D1RenderTarget interface [Direct2D]","ID2D1RenderTarget interface [Direct2D]","described","d2d1/ID2D1RenderTarget","direct2d.ID2D1RenderTarget"]
old-location: direct2d\ID2D1RenderTarget.htm
tech.root: Direct2D
ms.assetid: 40629be9-5840-4bde-b369-56bbfd791775
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget, ID2D1RenderTarget interface [Direct2D], ID2D1RenderTarget interface [Direct2D],described, d2d1/ID2D1RenderTarget, direct2d.ID2D1RenderTarget
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget
 - d2d1/ID2D1RenderTarget
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
 - ID2D1RenderTarget
---

# ID2D1RenderTarget interface


## -description

Represents an object that can receive drawing commands. Interfaces that inherit from <b>ID2D1RenderTarget</b> render the drawing commands they receive in different ways.

## -inheritance

The <b>ID2D1RenderTarget</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1RenderTarget</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created).

## -see-also

<a href="/windows/win32/Direct2D/the-direct2d-api">Direct2D API Overview</a>



<a href="/windows/win32/Direct2D/getting-started-with-direct2d-nav">Getting Started</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

