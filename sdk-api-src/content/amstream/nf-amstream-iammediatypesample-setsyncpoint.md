---
UID: NF:amstream.IAMMediaTypeSample.SetSyncPoint
title: IAMMediaTypeSample::SetSyncPoint (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetSyncPoint method specifies whether the beginning of this sample is a synchronization point.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetSyncPoint method","IAMMediaTypeSample.SetSyncPoint","IAMMediaTypeSample::SetSyncPoint","IAMMediaTypeSampleSetSyncPoint","SetSyncPoint","SetSyncPoint method [DirectShow]","SetSyncPoint method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetSyncPoint","dshow.iammediatypesample_setsyncpoint"]
old-location: dshow\iammediatypesample_setsyncpoint.htm
tech.root: dshow
ms.assetid: d2ff9b33-c49c-4715-b580-f05670a0f405
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetSyncPoint method, IAMMediaTypeSample.SetSyncPoint, IAMMediaTypeSample::SetSyncPoint, IAMMediaTypeSampleSetSyncPoint, SetSyncPoint, SetSyncPoint method [DirectShow], SetSyncPoint method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetSyncPoint, dshow.iammediatypesample_setsyncpoint
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
 - IAMMediaTypeSample::SetSyncPoint
 - amstream/IAMMediaTypeSample::SetSyncPoint
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
 - IAMMediaTypeSample.SetSyncPoint
---

# IAMMediaTypeSample::SetSyncPoint


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetSyncPoint</code> method specifies whether the beginning of this sample is a synchronization point.

## -parameters

### -param bIsSyncPoint

Boolean value that specifies whether the beginning of this sample is a synchronization point. If <b>TRUE</b>, the beginning of the sample is a synchronization point.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>