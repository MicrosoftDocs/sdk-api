---
UID: NF:il21dec.IAMLine21Decoder.SetBackgroundColor
title: IAMLine21Decoder::SetBackgroundColor (il21dec.h)
description: The SetBackgroundColor method sets the background color that the Line 21 Decoder filter uses for overlay. The default background color is magenta.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetBackgroundColor method","IAMLine21Decoder.SetBackgroundColor","IAMLine21Decoder::SetBackgroundColor","IAMLine21DecoderSetBackgroundColor","SetBackgroundColor","SetBackgroundColor method [DirectShow]","SetBackgroundColor method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setbackgroundcolor","il21dec/IAMLine21Decoder::SetBackgroundColor"]
old-location: dshow\iamline21decoder_setbackgroundcolor.htm
tech.root: dshow
ms.assetid: a69bb0d0-5afb-420f-a97c-071dc472e1d2
ms.date: 12/05/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetBackgroundColor method, IAMLine21Decoder.SetBackgroundColor, IAMLine21Decoder::SetBackgroundColor, IAMLine21DecoderSetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DirectShow], SetBackgroundColor method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setbackgroundcolor, il21dec/IAMLine21Decoder::SetBackgroundColor
req.header: il21dec.h
req.include-header: 
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
 - IAMLine21Decoder::SetBackgroundColor
 - il21dec/IAMLine21Decoder::SetBackgroundColor
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
 - IAMLine21Decoder.SetBackgroundColor
---

# IAMLine21Decoder::SetBackgroundColor


## -description

The <code>SetBackgroundColor</code> method sets the background color that the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter uses for overlay. The default background color is magenta.



Generally, applications should not call this method. The background color must match the overlay color key, which is defined by the downstream rendering filter.

## -parameters

### -param dwPhysColor

Sets the background color as a pixel color value. The meaning of the pixel value is defined by the bit depth of the filter's current output format.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getbackgroundcolor">IAMLine21Decoder::GetBackgroundColor</a>