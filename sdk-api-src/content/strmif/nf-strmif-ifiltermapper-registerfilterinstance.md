---
UID: NF:strmif.IFilterMapper.RegisterFilterInstance
title: IFilterMapper::RegisterFilterInstance (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Registers an identifiable instance of a filter.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","RegisterFilterInstance method","IFilterMapper.RegisterFilterInstance","IFilterMapper::RegisterFilterInstance","IFilterMapperRegisterFilterInstance","RegisterFilterInstance","RegisterFilterInstance method [DirectShow]","RegisterFilterInstance method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_registerfilterinstance","strmif/IFilterMapper::RegisterFilterInstance"]
old-location: dshow\ifiltermapper_registerfilterinstance.htm
tech.root: dshow
ms.assetid: ce42047c-0b74-4ad4-b5a1-ea66fc6bffc3
ms.date: 4/26/2023
ms.keywords: IFilterMapper interface [DirectShow],RegisterFilterInstance method, IFilterMapper.RegisterFilterInstance, IFilterMapper::RegisterFilterInstance, IFilterMapperRegisterFilterInstance, RegisterFilterInstance, RegisterFilterInstance method [DirectShow], RegisterFilterInstance method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerfilterinstance, strmif/IFilterMapper::RegisterFilterInstance
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
 - IFilterMapper::RegisterFilterInstance
 - strmif/IFilterMapper::RegisterFilterInstance
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
 - IFilterMapper.RegisterFilterInstance
---

# IFilterMapper::RegisterFilterInstance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Registers an identifiable instance of a filter.

## -parameters

### -param clsid [in]

GUID of the filter.

### -param Name [in]

Descriptive name of the instance.

### -param MRId [out]

Pointer to the returned media resource ID. This parameter is a locally unique identifier for this instance of this filter.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method handles cases such as when two similar sound cards that are driven by the same driver are available, and it is necessary to choose which card will emit the sound. This is not needed if there is only one instance of the filter (such as when there is only one sound card in the computer), or if all instances of the filter are equivalent.

The filter itself must have already been registered.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>