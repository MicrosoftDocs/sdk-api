---
UID: NF:d2d1effectauthor.ID2D1RenderInfo.SetInputDescription
title: ID2D1RenderInfo::SetInputDescription (d2d1effectauthor.h)
description: Sets how a specific input to the transform should be handled by the renderer in terms of sampling.
helpviewer_keywords: ["ID2D1RenderInfo interface [Direct2D]","SetInputDescription method","ID2D1RenderInfo.SetInputDescription","ID2D1RenderInfo::SetInputDescription","SetInputDescription","SetInputDescription method [Direct2D]","SetInputDescription method [Direct2D]","ID2D1RenderInfo interface","d2d1effectauthor/ID2D1RenderInfo::SetInputDescription","direct2d.id2d1renderinfo_setinputdescription"]
old-location: direct2d\id2d1renderinfo_setinputdescription.htm
tech.root: Direct2D
ms.assetid: 31571676-7030-4FBB-BDED-3CE3BA7E7CE6
ms.date: 12/05/2018
ms.keywords: ID2D1RenderInfo interface [Direct2D],SetInputDescription method, ID2D1RenderInfo.SetInputDescription, ID2D1RenderInfo::SetInputDescription, SetInputDescription, SetInputDescription method [Direct2D], SetInputDescription method [Direct2D],ID2D1RenderInfo interface, d2d1effectauthor/ID2D1RenderInfo::SetInputDescription, direct2d.id2d1renderinfo_setinputdescription
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderInfo::SetInputDescription
 - d2d1effectauthor/ID2D1RenderInfo::SetInputDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1RenderInfo.SetInputDescription
---

# ID2D1RenderInfo::SetInputDescription


## -description

Sets how a specific input to the transform should be handled by the renderer in terms of sampling.

## -parameters

### -param inputIndex

Type: <b>UINT32</b>

The index of the input that will have the input description applied.

### -param inputDescription

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description">D2D1_INPUT_DESCRIPTION</a></b>

The description of the input to be applied to the transform.

## -returns

Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


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
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -remarks

The input description must be matched correctly by the effect shader code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a>



<a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_channel_depth">D2D1_CHANNEL_DEPTH</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls_)">ID2D1DeviceContext::SetRenderingControls</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1renderinfo">ID2D1RenderInfo</a>