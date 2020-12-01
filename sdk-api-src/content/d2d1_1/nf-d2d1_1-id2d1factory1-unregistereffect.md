---
UID: NF:d2d1_1.ID2D1Factory1.UnregisterEffect
title: ID2D1Factory1::UnregisterEffect (d2d1_1.h)
description: Unregisters an effect within the factory instance that corresponds to the classId provided.
helpviewer_keywords: ["ID2D1Factory1 interface [Direct2D]","UnregisterEffect method","ID2D1Factory1.UnregisterEffect","ID2D1Factory1::UnregisterEffect","UnregisterEffect","UnregisterEffect method [Direct2D]","UnregisterEffect method [Direct2D]","ID2D1Factory1 interface","d2d1_1/ID2D1Factory1::UnregisterEffect","direct2d.id2d1factory1_unregistereffect"]
old-location: direct2d\id2d1factory1_unregistereffect.htm
tech.root: Direct2D
ms.assetid: 5f383406-5d83-4ccc-9082-526b9e9fa80b
ms.date: 12/05/2018
ms.keywords: ID2D1Factory1 interface [Direct2D],UnregisterEffect method, ID2D1Factory1.UnregisterEffect, ID2D1Factory1::UnregisterEffect, UnregisterEffect, UnregisterEffect method [Direct2D], UnregisterEffect method [Direct2D],ID2D1Factory1 interface, d2d1_1/ID2D1Factory1::UnregisterEffect, direct2d.id2d1factory1_unregistereffect
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::UnregisterEffect
 - d2d1_1/ID2D1Factory1::UnregisterEffect
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
 - ID2D1Factory1.UnregisterEffect
---

# ID2D1Factory1::UnregisterEffect


## -description

Unregisters an  effect within the factory instance that corresponds to the <i>classId</i> provided.

## -parameters

### -param classId [in]

Type: <b>REFCLSID</b>

The identifier of the effect to be unregistered.

## -returns

Type: <b>HRESULT</b>

D2DERR_EFFECT_IS_NOT_REGISTERED if the effect is not registered, S_OK otherwise.

## -remarks

In order for the effect to be fully unloaded, you must call <b>UnregisterEffect</b> the same number of times that you have registered the effect.

The <b>UnregisterEffect</b> method unregisters only those effects that are registered on the same factory. It cannot be used to unregister a built-in effect.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">ID2D1Factory1::RegisterEffect</a>