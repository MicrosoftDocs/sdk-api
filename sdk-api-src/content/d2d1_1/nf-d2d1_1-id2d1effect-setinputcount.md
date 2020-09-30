---
UID: NF:d2d1_1.ID2D1Effect.SetInputCount
title: ID2D1Effect::SetInputCount (d2d1_1.h)
description: Allows the application to change the number of inputs to an effect.
helpviewer_keywords: ["ID2D1Effect interface [Direct2D]","SetInputCount method","ID2D1Effect.SetInputCount","ID2D1Effect::SetInputCount","SetInputCount","SetInputCount method [Direct2D]","SetInputCount method [Direct2D]","ID2D1Effect interface","d2d1_1/ID2D1Effect::SetInputCount","direct2d.id2d1effect_setnumberofinputs"]
old-location: direct2d\id2d1effect_setnumberofinputs.htm
tech.root: Direct2D
ms.assetid: cdcaa997-acbe-40e3-9439-629b3853d8d4
ms.date: 12/05/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInputCount method, ID2D1Effect.SetInputCount, ID2D1Effect::SetInputCount, SetInputCount, SetInputCount method [Direct2D], SetInputCount method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInputCount, direct2d.id2d1effect_setnumberofinputs
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
 - ID2D1Effect::SetInputCount
 - d2d1_1/ID2D1Effect::SetInputCount
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
 - ID2D1Effect.SetInputCount
---

# ID2D1Effect::SetInputCount


## -description

Allows the application to change the number of inputs to an effect.

## -parameters

### -param inputCount

Type: <b>UINT32</b>

The number of inputs to the effect.

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
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Failed to allocate necessary memory.</td>
</tr>
</table>

## -remarks

Most effects do not support a variable number of inputs. Use <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)">ID2D1Properties::GetValue</a> with the <b>D2D1_PROPERTY_MIN_INPUTS</b> and <b>D2D1_PROPERTY_MAX_INPUTS</b> values to determine the number of inputs supported by an effect.

If the input count is less than the minimum or more than the maximum supported inputs, the call will fail.

If the input count is unchanged, the call will succeed with <b>S_OK</b>. 

Any inputs currently selected on the effect will be unaltered by this call unless the number of inputs is made smaller. If the number of inputs is made smaller, inputs beyond the selected range will be released.

If the method fails, the existing input and input count will remain unchanged.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput">ID2D1Effect::GetOutput</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>