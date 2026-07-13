---
UID: NF:strmif.IAMPushSource.GetStreamOffset
title: IAMPushSource::GetStreamOffset (strmif.h)
description: The GetStreamOffset method retrieves the offset that the filter uses when generating time stamps.
helpviewer_keywords: ["GetStreamOffset","GetStreamOffset method [DirectShow]","GetStreamOffset method [DirectShow]","IAMPushSource interface","IAMPushSource interface [DirectShow]","GetStreamOffset method","IAMPushSource.GetStreamOffset","IAMPushSource::GetStreamOffset","IAMPushSourceGetStreamOffset","dshow.iampushsource_getstreamoffset","strmif/IAMPushSource::GetStreamOffset"]
old-location: dshow\iampushsource_getstreamoffset.htm
tech.root: dshow
ms.assetid: 249d5262-e02d-4df7-a968-0680b64ab7d4
ms.date: 4/26/2023
ms.keywords: GetStreamOffset, GetStreamOffset method [DirectShow], GetStreamOffset method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetStreamOffset method, IAMPushSource.GetStreamOffset, IAMPushSource::GetStreamOffset, IAMPushSourceGetStreamOffset, dshow.iampushsource_getstreamoffset, strmif/IAMPushSource::GetStreamOffset
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMPushSource::GetStreamOffset
 - strmif/IAMPushSource::GetStreamOffset
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
 - IAMPushSource.GetStreamOffset
---

# IAMPushSource::GetStreamOffset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStreamOffset</code> method retrieves the offset that the filter uses when generating time stamps.

## -parameters

### -param prtOffset [out]

Pointer to a variable that receives a reference time indicating the current stream offset.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>