---
UID: NF:amvideo.IQualProp.get_FramesDroppedInRenderer
title: IQualProp::get_FramesDroppedInRenderer (amvideo.h)
description: The get_FramesDroppedInRenderer method retrieves the number of frames dropped by the renderer.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_FramesDroppedInRenderer method","IQualProp.get_FramesDroppedInRenderer","IQualProp::get_FramesDroppedInRenderer","IQualPropget_FramesDroppedInRenderer","amvideo/IQualProp::get_FramesDroppedInRenderer","dshow.iqualprop_get_framesdroppedinrenderer","get_FramesDroppedInRenderer","get_FramesDroppedInRenderer method [DirectShow]","get_FramesDroppedInRenderer method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_framesdroppedinrenderer.htm
tech.root: dshow
ms.assetid: 342aff30-ed1c-406d-8fbe-0524acbcd2d7
ms.date: 12/05/2018
ms.keywords: IQualProp interface [DirectShow],get_FramesDroppedInRenderer method, IQualProp.get_FramesDroppedInRenderer, IQualProp::get_FramesDroppedInRenderer, IQualPropget_FramesDroppedInRenderer, amvideo/IQualProp::get_FramesDroppedInRenderer, dshow.iqualprop_get_framesdroppedinrenderer, get_FramesDroppedInRenderer, get_FramesDroppedInRenderer method [DirectShow], get_FramesDroppedInRenderer method [DirectShow],IQualProp interface
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQualProp::get_FramesDroppedInRenderer
 - amvideo/IQualProp::get_FramesDroppedInRenderer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQualProp.get_FramesDroppedInRenderer
---

# IQualProp::get_FramesDroppedInRenderer


## -description

The <code>get_FramesDroppedInRenderer</code> method retrieves the number of frames dropped by the renderer.

## -parameters

### -param pcFrames

Pointer to the number of frames dropped by the renderer.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The property page uses this method to retrieve data from the renderer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>