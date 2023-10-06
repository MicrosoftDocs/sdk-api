---
UID: NF:amstream.IAMMediaTypeSample.GetPointer
title: IAMMediaTypeSample::GetPointer (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetPointer method retrieves a read/write pointer to the buffer's memory.
helpviewer_keywords: ["GetPointer","GetPointer method [DirectShow]","GetPointer method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetPointer method","IAMMediaTypeSample.GetPointer","IAMMediaTypeSample::GetPointer","IAMMediaTypeSampleGetPointer","amstream/IAMMediaTypeSample::GetPointer","dshow.iammediatypesample_getpointer"]
old-location: dshow\iammediatypesample_getpointer.htm
tech.root: dshow
ms.assetid: e1ca46d8-51d6-4dd5-bbcc-463acf53420c
ms.date: 4/26/2023
ms.keywords: GetPointer, GetPointer method [DirectShow], GetPointer method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetPointer method, IAMMediaTypeSample.GetPointer, IAMMediaTypeSample::GetPointer, IAMMediaTypeSampleGetPointer, amstream/IAMMediaTypeSample::GetPointer, dshow.iammediatypesample_getpointer
req.header: amstream.h
req.include-header: 
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
 - IAMMediaTypeSample::GetPointer
 - amstream/IAMMediaTypeSample::GetPointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.GetPointer
---

# IAMMediaTypeSample::GetPointer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetPointer</code> method retrieves a read/write pointer to the buffer's memory.

## -parameters

### -param ppBuffer [out]

Address of a pointer to the buffer.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>