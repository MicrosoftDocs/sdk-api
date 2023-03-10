---
UID: NF:d2d1.ID2D1RenderTarget.GetTags
title: ID2D1RenderTarget::GetTags (d2d1.h)
description: Gets the label for subsequent drawing operations.
helpviewer_keywords: ["GetTags","GetTags method [Direct2D]","GetTags method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","GetTags method","ID2D1RenderTarget.GetTags","ID2D1RenderTarget::GetTags","d2d1/ID2D1RenderTarget::GetTags","direct2d.ID2D1RenderTarget_GetTags"]
old-location: direct2d\ID2D1RenderTarget_GetTags.htm
tech.root: Direct2D
ms.assetid: 71da439f-4666-4e49-93f8-26acd222ed1e
ms.date: 12/05/2018
ms.keywords: GetTags, GetTags method [Direct2D], GetTags method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetTags method, ID2D1RenderTarget.GetTags, ID2D1RenderTarget::GetTags, d2d1/ID2D1RenderTarget::GetTags, direct2d.ID2D1RenderTarget_GetTags
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
 - ID2D1RenderTarget::GetTags
 - d2d1/ID2D1RenderTarget::GetTags
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
 - ID2D1RenderTarget.GetTags
---

# ID2D1RenderTarget::GetTags


## -description

Gets the label for subsequent drawing operations.

## -parameters

### -param tag1 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the first label for subsequent drawing operations. This parameter is passed uninitialized. If <b>NULL</b> is specified, no value is retrieved for this parameter.

### -param tag2 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the second label for subsequent drawing operations. This parameter is passed uninitialized. If <b>NULL</b> is specified, no value is retrieved for this parameter.

## -remarks

If the same address is passed for both parameters, both parameters receive the value of the second tag.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

