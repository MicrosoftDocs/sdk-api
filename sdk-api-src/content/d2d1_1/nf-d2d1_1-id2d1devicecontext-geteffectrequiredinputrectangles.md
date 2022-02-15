---
UID: NF:d2d1_1.ID2D1DeviceContext.GetEffectRequiredInputRectangles
title: ID2D1DeviceContext::GetEffectRequiredInputRectangles (d2d1_1.h)
description: Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle.
helpviewer_keywords: ["GetEffectRequiredInputRectangles","GetEffectRequiredInputRectangles method [Direct2D]","GetEffectRequiredInputRectangles method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetEffectRequiredInputRectangles method","ID2D1DeviceContext.GetEffectRequiredInputRectangles","ID2D1DeviceContext::GetEffectRequiredInputRectangles","d2d1_1/ID2D1DeviceContext::GetEffectRequiredInputRectangles","direct2d.id2d1devicecontext_geteffectrequiredinputrectangles"]
old-location: direct2d\id2d1devicecontext_geteffectrequiredinputrectangles.htm
tech.root: Direct2D
ms.assetid: B34548A9-1E23-496F-A1D9-87B74EF67C72
ms.date: 12/05/2018
ms.keywords: GetEffectRequiredInputRectangles, GetEffectRequiredInputRectangles method [Direct2D], GetEffectRequiredInputRectangles method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetEffectRequiredInputRectangles method, ID2D1DeviceContext.GetEffectRequiredInputRectangles, ID2D1DeviceContext::GetEffectRequiredInputRectangles, d2d1_1/ID2D1DeviceContext::GetEffectRequiredInputRectangles, direct2d.id2d1devicecontext_geteffectrequiredinputrectangles
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
 - ID2D1DeviceContext::GetEffectRequiredInputRectangles
 - d2d1_1/ID2D1DeviceContext::GetEffectRequiredInputRectangles
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
 - ID2D1DeviceContext.GetEffectRequiredInputRectangles
---

# ID2D1DeviceContext::GetEffectRequiredInputRectangles


## -description

Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle.

## -parameters

### -param renderEffect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The image whose output is being rendered.

### -param renderImageRectangle [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The portion of the output image whose inputs are being inspected.

### -param inputDescriptions [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_effect_input_description">D2D1_EFFECT_INPUT_DESCRIPTION</a>*</b>

A list of the inputs whose rectangles are being queried.

### -param requiredInputRects [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The input rectangles returned to the caller.

### -param inputCount

Type: <b>UINT32</b>

The number of inputs.

## -returns

Type: <b>HRESULT</b>

A failure code, this will typically only be because an effect in the chain returned some error.

## -remarks

The caller should be very careful not to place a reliance on the required input rectangles returned. 
      Small changes for correctness to an effect's behavior can result in different rectangles being returned. 
      In addition, different kinds of optimization applied inside the render can also influence the result.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>