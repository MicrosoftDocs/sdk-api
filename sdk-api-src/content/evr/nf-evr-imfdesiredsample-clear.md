---
UID: NF:evr.IMFDesiredSample.Clear
title: IMFDesiredSample::Clear (evr.h)
description: Clears the time stamps previously set by a call to IMFDesiredSample::SetDesiredSampleTimeAndDuration.
helpviewer_keywords: ["Clear","Clear method [Media Foundation]","Clear method [Media Foundation]","IMFDesiredSample interface","IMFDesiredSample interface [Media Foundation]","Clear method","IMFDesiredSample.Clear","IMFDesiredSample::Clear","d5c6c1c2-c122-47b6-82b3-28b54bafc7b8","evr/IMFDesiredSample::Clear","mf.imfdesiredsample_clear"]
old-location: mf\imfdesiredsample_clear.htm
tech.root: mfarchive
ms.assetid: d5c6c1c2-c122-47b6-82b3-28b54bafc7b8
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Media Foundation], Clear method [Media Foundation],IMFDesiredSample interface, IMFDesiredSample interface [Media Foundation],Clear method, IMFDesiredSample.Clear, IMFDesiredSample::Clear, d5c6c1c2-c122-47b6-82b3-28b54bafc7b8, evr/IMFDesiredSample::Clear, mf.imfdesiredsample_clear
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFDesiredSample::Clear
 - evr/IMFDesiredSample::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFDesiredSample.Clear
archived: true
---

# IMFDesiredSample::Clear


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Clears the time stamps previously set by a call to <a href="/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration">IMFDesiredSample::SetDesiredSampleTimeAndDuration</a>.



## -remarks

After this method is called, the <a href="/windows/desktop/api/evr/nf-evr-imfdesiredsample-getdesiredsampletimeandduration">IMFDesiredSample::GetDesiredSampleTimeAndDuration</a> method returns MF_E_NOT_AVAILABLE.

This method also clears the time stamp and duration and removes all attributes from the sample.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>
