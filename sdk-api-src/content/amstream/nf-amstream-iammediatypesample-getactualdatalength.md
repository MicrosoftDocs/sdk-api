---
UID: NF:amstream.IAMMediaTypeSample.GetActualDataLength
title: IAMMediaTypeSample::GetActualDataLength (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetActualDataLength method retrieves the data length of the sample, in bytes.
helpviewer_keywords: ["GetActualDataLength","GetActualDataLength method [DirectShow]","GetActualDataLength method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetActualDataLength method","IAMMediaTypeSample.GetActualDataLength","IAMMediaTypeSample::GetActualDataLength","IAMMediaTypeSampleGetActualDataLength","amstream/IAMMediaTypeSample::GetActualDataLength","dshow.iammediatypesample_getactualdatalength"]
old-location: dshow\iammediatypesample_getactualdatalength.htm
tech.root: dshow
ms.assetid: e73672c7-7400-40dd-be65-f6c30c476c91
ms.date: 4/26/2023
ms.keywords: GetActualDataLength, GetActualDataLength method [DirectShow], GetActualDataLength method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetActualDataLength method, IAMMediaTypeSample.GetActualDataLength, IAMMediaTypeSample::GetActualDataLength, IAMMediaTypeSampleGetActualDataLength, amstream/IAMMediaTypeSample::GetActualDataLength, dshow.iammediatypesample_getactualdatalength
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
 - IAMMediaTypeSample::GetActualDataLength
 - amstream/IAMMediaTypeSample::GetActualDataLength
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
 - IAMMediaTypeSample.GetActualDataLength
---

# IAMMediaTypeSample::GetActualDataLength


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetActualDataLength</code> method retrieves the data length of the sample, in bytes.



## -returns

Returns the data length of the sample, in bytes.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
