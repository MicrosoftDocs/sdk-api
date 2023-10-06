---
UID: NF:amstream.IAMMediaTypeSample.IsSyncPoint
title: IAMMediaTypeSample::IsSyncPoint (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IsSyncPoint method determines if the beginning of a sample is a synchronization point.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","IsSyncPoint method","IAMMediaTypeSample.IsSyncPoint","IAMMediaTypeSample::IsSyncPoint","IAMMediaTypeSampleIsSyncPoint","IsSyncPoint","IsSyncPoint method [DirectShow]","IsSyncPoint method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::IsSyncPoint","dshow.iammediatypesample_issyncpoint"]
old-location: dshow\iammediatypesample_issyncpoint.htm
tech.root: dshow
ms.assetid: 0494f51e-2602-4574-88dd-0839a1d2f04f
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],IsSyncPoint method, IAMMediaTypeSample.IsSyncPoint, IAMMediaTypeSample::IsSyncPoint, IAMMediaTypeSampleIsSyncPoint, IsSyncPoint, IsSyncPoint method [DirectShow], IsSyncPoint method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::IsSyncPoint, dshow.iammediatypesample_issyncpoint
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
 - IAMMediaTypeSample::IsSyncPoint
 - amstream/IAMMediaTypeSample::IsSyncPoint
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
 - IAMMediaTypeSample.IsSyncPoint
---

# IAMMediaTypeSample::IsSyncPoint


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

> [!NOTE]
>  This interface is deprecated. New applications should not use it.

The <code>IsSyncPoint</code> method determines if the beginning of a sample is a synchronization point.



## -returns

Returns S_OK if the beginning of the sample is a synchronization point, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
