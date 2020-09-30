---
UID: NF:d2d1_1.ID2D1Effect.SetInputEffect
title: ID2D1Effect::SetInputEffect (d2d1_1.h)
description: Sets the given input effect by index.
helpviewer_keywords: ["ID2D1Effect interface [Direct2D]","SetInputEffect method","ID2D1Effect.SetInputEffect","ID2D1Effect::SetInputEffect","SetInputEffect","SetInputEffect method [Direct2D]","SetInputEffect method [Direct2D]","ID2D1Effect interface","d2d1_1/ID2D1Effect::SetInputEffect","direct2d.id2d1effect_setinputeffect"]
old-location: direct2d\id2d1effect_setinputeffect.htm
tech.root: Direct2D
ms.assetid: 361B0644-7437-47DA-A34C-0234EE4E92C3
ms.date: 12/05/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInputEffect method, ID2D1Effect.SetInputEffect, ID2D1Effect::SetInputEffect, SetInputEffect, SetInputEffect method [Direct2D], SetInputEffect method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInputEffect, direct2d.id2d1effect_setinputeffect
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
 - ID2D1Effect::SetInputEffect
 - d2d1_1/ID2D1Effect::SetInputEffect
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
 - ID2D1Effect.SetInputEffect
---

# ID2D1Effect::SetInputEffect


## -description

Sets the given input effect by index. 

This method gets the output of the given effect and then passes the output image to the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput">SetInput</a> method.

## -parameters

### -param index

The index of the input to set.

### -param inputEffect [in, optional]

The input effect to set.

### -param invalidate

Whether to invalidate the graph at the location of the effect input

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput">ID2D1Effect::GetOutput</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>