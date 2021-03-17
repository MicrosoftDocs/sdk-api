---
UID: NF:d2d1.ID2D1RenderTarget.SetTags
title: ID2D1RenderTarget::SetTags (d2d1.h)
description: Specifies a label for subsequent drawing operations.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","SetTags method","ID2D1RenderTarget.SetTags","ID2D1RenderTarget::SetTags","SetTags","SetTags method [Direct2D]","SetTags method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::SetTags","direct2d.ID2D1RenderTarget_SetTags"]
old-location: direct2d\ID2D1RenderTarget_SetTags.htm
tech.root: Direct2D
ms.assetid: d71c3500-e11f-4b2d-9b78-b57df7dbc2bd
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetTags method, ID2D1RenderTarget.SetTags, ID2D1RenderTarget::SetTags, SetTags, SetTags method [Direct2D], SetTags method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetTags, direct2d.ID2D1RenderTarget_SetTags
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
 - ID2D1RenderTarget::SetTags
 - d2d1/ID2D1RenderTarget::SetTags
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
 - ID2D1RenderTarget.SetTags
---

# ID2D1RenderTarget::SetTags


## -description

Specifies a label for subsequent drawing operations.

## -parameters

### -param tag1

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label to apply to subsequent drawing operations.

### -param tag2

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label to apply to subsequent drawing operations.

## -remarks

The labels specified by this method are printed by debug error messages. If no tag is set, the default value for each tag is 0.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

