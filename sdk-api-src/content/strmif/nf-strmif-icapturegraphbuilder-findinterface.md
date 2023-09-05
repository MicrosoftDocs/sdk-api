---
UID: NF:strmif.ICaptureGraphBuilder.FindInterface
title: ICaptureGraphBuilder::FindInterface (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.
helpviewer_keywords: ["FindInterface","FindInterface method [DirectShow]","FindInterface method [DirectShow]","ICaptureGraphBuilder interface","ICaptureGraphBuilder interface [DirectShow]","FindInterface method","ICaptureGraphBuilder.FindInterface","ICaptureGraphBuilder::FindInterface","ICaptureGraphBuilderFindInterface","dshow.icapturegraphbuilder_findinterface","strmif/ICaptureGraphBuilder::FindInterface"]
old-location: dshow\icapturegraphbuilder_findinterface.htm
tech.root: dshow
ms.assetid: 23fe9a5a-0f3b-44b3-9d37-6889214657bf
ms.date: 4/26/2023
ms.keywords: FindInterface, FindInterface method [DirectShow], FindInterface method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],FindInterface method, ICaptureGraphBuilder.FindInterface, ICaptureGraphBuilder::FindInterface, ICaptureGraphBuilderFindInterface, dshow.icapturegraphbuilder_findinterface, strmif/ICaptureGraphBuilder::FindInterface
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
 - ICaptureGraphBuilder::FindInterface
 - strmif/ICaptureGraphBuilder::FindInterface
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
 - ICaptureGraphBuilder.FindInterface
---

# ICaptureGraphBuilder::FindInterface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.

## -parameters

### -param pCategory [in]

Pointer to a GUID specifying the output pin category. See <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a> for a list of all pin categories. <b>NULL</b> indicates search all the output pins regardless of category.

### -param pf [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter.

### -param riid [in]

Reference ID of the desired interface.

### -param ppint [out]

Address of a void pointer. If the interface was found, this method initializes <i>ppint</i> so that it contains the address of a pointer to the found interface. Call the <b>Release</b> method to decrement the reference count when you're done with the interface.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method looks for the interface on the filter, and upstream and downstream of the filter, unless a category is given. If a category is given, it only looks downstream of the output pin of that category. It can be used to find interfaces on renderers, multiplexers, TV tuners, crossbars, and so forth.

If <i>pCategory</i> equals &amp;LOOK_UPSTREAM_ONLY, then the graph builder will look upstream of the filter given in parameter <i>pf</i>, but not on the filter itself, nor downstream of the filter.

If <i>pCategory</i> equals &amp;LOOK_DOWNSTREAM_ONLY, then the graph builder will look downstream of the filter given in parameter <i>pf</i>, but not on the filter itself, nor upstream of the filter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>