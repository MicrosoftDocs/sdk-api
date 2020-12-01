---
UID: NF:d2d1_1.ID2D1Effect.GetOutput
title: ID2D1Effect::GetOutput (d2d1_1.h)
description: Gets the output image from the effect.
helpviewer_keywords: ["GetOutput","GetOutput method [Direct2D]","GetOutput method [Direct2D]","ID2D1Effect interface","ID2D1Effect interface [Direct2D]","GetOutput method","ID2D1Effect.GetOutput","ID2D1Effect::GetOutput","d2d1_1/ID2D1Effect::GetOutput","direct2d.id2d1effect_getoutput"]
old-location: direct2d\id2d1effect_getoutput.htm
tech.root: Direct2D
ms.assetid: e14066f7-b195-44f1-a952-1b6c9f3832cf
ms.date: 12/05/2018
ms.keywords: GetOutput, GetOutput method [Direct2D], GetOutput method [Direct2D],ID2D1Effect interface, ID2D1Effect interface [Direct2D],GetOutput method, ID2D1Effect.GetOutput, ID2D1Effect::GetOutput, d2d1_1/ID2D1Effect::GetOutput, direct2d.id2d1effect_getoutput
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
 - ID2D1Effect::GetOutput
 - d2d1_1/ID2D1Effect::GetOutput
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
 - ID2D1Effect.GetOutput
---

# ID2D1Effect::GetOutput


## -description

Gets the output image from the effect.

## -parameters

### -param outputImage [out]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>**</b>

When this method returns, contains the address of a pointer to the output image for the effect.

## -remarks

The output image  can be set as an input to another effect, or can be directly passed into the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> in order to render the effect. 

It is  also possible to use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to retrieve the same output image.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput">ID2D1Effect::GetOutput</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>