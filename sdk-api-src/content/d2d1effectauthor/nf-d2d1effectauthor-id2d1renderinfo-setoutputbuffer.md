---
UID: NF:d2d1effectauthor.ID2D1RenderInfo.SetOutputBuffer
title: ID2D1RenderInfo::SetOutputBuffer (d2d1effectauthor.h)
description: Allows a caller to control the output precision and channel-depth of the transform in which the render information is encapsulated.
helpviewer_keywords: ["ID2D1RenderInfo interface [Direct2D]","SetOutputBuffer method","ID2D1RenderInfo.SetOutputBuffer","ID2D1RenderInfo::SetOutputBuffer","SetOutputBuffer","SetOutputBuffer method [Direct2D]","SetOutputBuffer method [Direct2D]","ID2D1RenderInfo interface","d2d1effectauthor/ID2D1RenderInfo::SetOutputBuffer","direct2d.id2d1renderinfo_setoutputbuffer"]
old-location: direct2d\id2d1renderinfo_setoutputbuffer.htm
tech.root: Direct2D
ms.assetid: 4267FCA0-10AF-4731-8B68-B3425FA00185
ms.date: 12/05/2018
ms.keywords: ID2D1RenderInfo interface [Direct2D],SetOutputBuffer method, ID2D1RenderInfo.SetOutputBuffer, ID2D1RenderInfo::SetOutputBuffer, SetOutputBuffer, SetOutputBuffer method [Direct2D], SetOutputBuffer method [Direct2D],ID2D1RenderInfo interface, d2d1effectauthor/ID2D1RenderInfo::SetOutputBuffer, direct2d.id2d1renderinfo_setoutputbuffer
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
 - ID2D1RenderInfo::SetOutputBuffer
 - d2d1effectauthor/ID2D1RenderInfo::SetOutputBuffer
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
 - ID2D1RenderInfo.SetOutputBuffer
---

# ID2D1RenderInfo::SetOutputBuffer


## -description

Allows a caller to control the output precision and channel-depth of the transform in which the render information is encapsulated.

## -parameters

### -param bufferPrecision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The type of buffer that should be used as an output from this transform.

### -param channelDepth

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_channel_depth">D2D1_CHANNEL_DEPTH</a></b>

The number of channels that will be used on the output buffer.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

 If the output precision of the transform is not specified, then it will default to the precision specified on the Direct2D device context. The maximum of 16bpc <b>UNORM</b> and 16bpc <b>FLOAT</b> is 32bpc <b>FLOAT</b>.

The output channel depth will match the maximum of the input channel depths if the channel depth is <b>D2D1_CHANNEL_DEPTH_DEFAULT</b>.

There is no global output channel depth, this is always left to the control of the transforms.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a>



<a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_channel_depth">D2D1_CHANNEL_DEPTH</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls_)">ID2D1DeviceContext::SetRenderingControls</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1renderinfo">ID2D1RenderInfo</a>