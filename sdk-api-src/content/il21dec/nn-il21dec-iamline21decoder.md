---
UID: NN:il21dec.IAMLine21Decoder
title: IAMLine21Decoder (il21dec.h)
description: The IAMLine21Decoder interface sets and retrieves information about closed captions.The Line 21 Decoder filter exposes this interface.
helpviewer_keywords: ["IAMLine21Decoder","IAMLine21Decoder interface [DirectShow]","IAMLine21Decoder interface [DirectShow]","described","IAMLine21DecoderInterface","dshow.iamline21decoder","il21dec/IAMLine21Decoder"]
old-location: dshow\iamline21decoder.htm
tech.root: dshow
ms.assetid: b6fbb5c3-28af-4db6-8dc4-82271b69bf71
ms.date: 12/05/2018
ms.keywords: IAMLine21Decoder, IAMLine21Decoder interface [DirectShow], IAMLine21Decoder interface [DirectShow],described, IAMLine21DecoderInterface, dshow.iamline21decoder, il21dec/IAMLine21Decoder
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
 - IAMLine21Decoder
 - il21dec/IAMLine21Decoder
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
 - IAMLine21Decoder
---

# IAMLine21Decoder interface


## -description

The <code>IAMLine21Decoder</code> interface sets and retrieves information about closed captions.

The <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter exposes this interface. Applications can use this interface to enable or disable closed captions, select the closed captioning service, and set other closed captioning properties.

Closed-captioned information is transmitted on line 21 of field 1 in the vertical blanking interval (VBI) of television signals. Video cassette recorders record this information on video tape, and you can use the Line21 Decoder and other DirectShow filters to capture the line 21 data and save it on disk in a media file format such as Audio-Video Interleaved (AVI). The closed-captioned information appears as a separate stream within the media file.

Closed-captioned text is used in television programming and DVD movies. DVD movies contain line 21 data as part of the user data section of each Group of Pictures (GOP) in the video stream. Television receiver cards with Windows Driver Model (WDM) drivers provide line 21 data.

## -inheritance

The <b>IAMLine21Decoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMLine21Decoder</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

