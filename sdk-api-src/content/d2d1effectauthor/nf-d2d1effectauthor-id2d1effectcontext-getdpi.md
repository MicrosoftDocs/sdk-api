---
UID: NF:d2d1effectauthor.ID2D1EffectContext.GetDpi
title: ID2D1EffectContext::GetDpi (d2d1effectauthor.h)
description: Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.
helpviewer_keywords: ["GetDpi","GetDpi method [Direct2D]","GetDpi method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","GetDpi method","ID2D1EffectContext.GetDpi","ID2D1EffectContext::GetDpi","d2d1effectauthor/ID2D1EffectContext::GetDpi","direct2d.id2d1contextinternal_getdpi"]
old-location: direct2d\id2d1contextinternal_getdpi.htm
tech.root: Direct2D
ms.assetid: 465D75BF-67A0-410C-950E-DB42995379B0
ms.date: 12/05/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],GetDpi method, ID2D1EffectContext.GetDpi, ID2D1EffectContext::GetDpi, d2d1effectauthor/ID2D1EffectContext::GetDpi, direct2d.id2d1contextinternal_getdpi
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
 - ID2D1EffectContext::GetDpi
 - d2d1effectauthor/ID2D1EffectContext::GetDpi
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
 - ID2D1EffectContext.GetDpi
---

# ID2D1EffectContext::GetDpi


## -description

Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.

## -parameters

### -param dpiX [out]

Type: <b>FLOAT*</b>

The dpi on the x-axis.

### -param dpiY [out]

Type: <b>FLOAT*</b>

The dpi on the y-axis.

## -remarks

 If the <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_unit_mode">D2D1_UNIT_MODE</a> is <b>D2D1_UNIT_MODE_PIXELS</b>, both <i>dpiX</i> and <i>dpiY</i> will be set to 96.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender">ID2D1EffectImpl::PrepareForRender</a>