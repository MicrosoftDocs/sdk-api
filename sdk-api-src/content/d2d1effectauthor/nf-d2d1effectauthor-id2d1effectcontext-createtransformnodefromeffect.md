---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateTransformNodeFromEffect
title: ID2D1EffectContext::CreateTransformNodeFromEffect (d2d1effectauthor.h)
description: Wraps an effect graph into a single transform node and then inserted into a transform graph. This allows an effect to aggregate other effects.
helpviewer_keywords: ["CreateTransformNodeFromEffect","CreateTransformNodeFromEffect method [Direct2D]","CreateTransformNodeFromEffect method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CreateTransformNodeFromEffect method","ID2D1EffectContext.CreateTransformNodeFromEffect","ID2D1EffectContext::CreateTransformNodeFromEffect","d2d1effectauthor/ID2D1EffectContext::CreateTransformNodeFromEffect","direct2d.id2d1contextinternal_createtransformnodefromeffect"]
old-location: direct2d\id2d1contextinternal_createtransformnodefromeffect.htm
tech.root: Direct2D
ms.assetid: 75F1366A-4E82-4CAD-A843-6E53035CB520
ms.date: 12/05/2018
ms.keywords: CreateTransformNodeFromEffect, CreateTransformNodeFromEffect method [Direct2D], CreateTransformNodeFromEffect method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateTransformNodeFromEffect method, ID2D1EffectContext.CreateTransformNodeFromEffect, ID2D1EffectContext::CreateTransformNodeFromEffect, d2d1effectauthor/ID2D1EffectContext::CreateTransformNodeFromEffect, direct2d.id2d1contextinternal_createtransformnodefromeffect
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
 - ID2D1EffectContext::CreateTransformNodeFromEffect
 - d2d1effectauthor/ID2D1EffectContext::CreateTransformNodeFromEffect
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
 - ID2D1EffectContext.CreateTransformNodeFromEffect
---

# ID2D1EffectContext::CreateTransformNodeFromEffect


## -description

Wraps an effect graph into a single transform node and then inserted into a transform graph. This allows an effect to aggregate other effects. This will typically be done in order to allow the effect properties to be re-expressed with a different contract, or to allow different components to integrate each-other’s effects.

## -parameters

### -param effect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The effect to be wrapped in a transform node.

### -param transformNode [out]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>**</b>

The returned transform node that encapsulates the effect graph.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>