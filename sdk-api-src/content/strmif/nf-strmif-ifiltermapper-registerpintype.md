---
UID: NF:strmif.IFilterMapper.RegisterPinType
title: IFilterMapper::RegisterPinType (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Registers this pin type.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","RegisterPinType method","IFilterMapper.RegisterPinType","IFilterMapper::RegisterPinType","IFilterMapperRegisterPinType","RegisterPinType","RegisterPinType method [DirectShow]","RegisterPinType method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_registerpintype","strmif/IFilterMapper::RegisterPinType"]
old-location: dshow\ifiltermapper_registerpintype.htm
tech.root: dshow
ms.assetid: 7f92745b-2b97-4cc6-9755-a580827b5bba
ms.date: 4/26/2023
ms.keywords: IFilterMapper interface [DirectShow],RegisterPinType method, IFilterMapper.RegisterPinType, IFilterMapper::RegisterPinType, IFilterMapperRegisterPinType, RegisterPinType, RegisterPinType method [DirectShow], RegisterPinType method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerpintype, strmif/IFilterMapper::RegisterPinType
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper::RegisterPinType
 - strmif/IFilterMapper::RegisterPinType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IFilterMapper.RegisterPinType
---

# IFilterMapper::RegisterPinType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Registers this pin type.

## -parameters

### -param clsFilter

Class identifier (CLSID) of the filter to which the pin belongs.

### -param strName

Name by which it is known.

### -param clsMajorType

Major type of the media sample supported by this pin class.

### -param clsSubType

Subtype of the media sample supported by this pin class.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <i>clsMajorType</i> and <i>clsSubType</i> parameters specify the media type of the pin and correspond to the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure's <b>majortype</b> and <b>subtype</b> members, respectively.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>