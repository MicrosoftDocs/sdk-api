---
UID: NF:strmif.ICaptureGraphBuilder.AllocCapFile
title: ICaptureGraphBuilder::AllocCapFile (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Preallocates a capture file to a specified size.
helpviewer_keywords: ["AllocCapFile","AllocCapFile method [DirectShow]","AllocCapFile method [DirectShow]","ICaptureGraphBuilder interface","ICaptureGraphBuilder interface [DirectShow]","AllocCapFile method","ICaptureGraphBuilder.AllocCapFile","ICaptureGraphBuilder::AllocCapFile","ICaptureGraphBuilderAllocCapFile","dshow.icapturegraphbuilder_alloccapfile","strmif/ICaptureGraphBuilder::AllocCapFile"]
old-location: dshow\icapturegraphbuilder_alloccapfile.htm
tech.root: dshow
ms.assetid: 116ee108-ae03-4761-84db-9391ebddaae2
ms.date: 4/26/2023
ms.keywords: AllocCapFile, AllocCapFile method [DirectShow], AllocCapFile method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],AllocCapFile method, ICaptureGraphBuilder.AllocCapFile, ICaptureGraphBuilder::AllocCapFile, ICaptureGraphBuilderAllocCapFile, dshow.icapturegraphbuilder_alloccapfile, strmif/ICaptureGraphBuilder::AllocCapFile
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
 - ICaptureGraphBuilder::AllocCapFile
 - strmif/ICaptureGraphBuilder::AllocCapFile
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
 - ICaptureGraphBuilder.AllocCapFile
---

# ICaptureGraphBuilder::AllocCapFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Preallocates a capture file to a specified size.

## -parameters

### -param lpstr [in]

Pointer to a wide-character string containing the name of the file to create or resize.

### -param dwlSize [in]

Size, in bytes, of the file to be allocated.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The call will fail if the file is read-only. For best capture results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>