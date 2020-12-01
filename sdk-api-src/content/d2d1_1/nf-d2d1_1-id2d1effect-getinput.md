---
UID: NF:d2d1_1.ID2D1Effect.GetInput
title: ID2D1Effect::GetInput (d2d1_1.h)
description: Gets the given input image by index.
helpviewer_keywords: ["GetInput","GetInput method [Direct2D]","GetInput method [Direct2D]","ID2D1Effect interface","ID2D1Effect interface [Direct2D]","GetInput method","ID2D1Effect.GetInput","ID2D1Effect::GetInput","d2d1_1/ID2D1Effect::GetInput","direct2d.id2d1effect_getinput"]
old-location: direct2d\id2d1effect_getinput.htm
tech.root: Direct2D
ms.assetid: fca22cc2-2299-4f74-8dc9-d931b899d4fb
ms.date: 12/05/2018
ms.keywords: GetInput, GetInput method [Direct2D], GetInput method [Direct2D],ID2D1Effect interface, ID2D1Effect interface [Direct2D],GetInput method, ID2D1Effect.GetInput, ID2D1Effect::GetInput, d2d1_1/ID2D1Effect::GetInput, direct2d.id2d1effect_getinput
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
 - ID2D1Effect::GetInput
 - d2d1_1/ID2D1Effect::GetInput
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
 - ID2D1Effect.GetInput
---

# ID2D1Effect::GetInput


## -description

Gets the given input image by index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the image to retrieve.

### -param input [out, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the image that is identified by <i>Index</i>.

## -remarks

If the input index is out of range, the returned image will be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput">ID2D1Effect::GetOutput</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>