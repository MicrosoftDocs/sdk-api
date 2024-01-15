---
UID: NF:evr.IMFDesiredSample.SetDesiredSampleTimeAndDuration
title: IMFDesiredSample::SetDesiredSampleTimeAndDuration (evr.h)
description: Called by the presenter to set the time and duration of the sample that it requests from the mixer.
helpviewer_keywords: ["12877b24-83ec-4156-b411-f07202fdfd62","IMFDesiredSample interface [Media Foundation]","SetDesiredSampleTimeAndDuration method","IMFDesiredSample.SetDesiredSampleTimeAndDuration","IMFDesiredSample::SetDesiredSampleTimeAndDuration","SetDesiredSampleTimeAndDuration","SetDesiredSampleTimeAndDuration method [Media Foundation]","SetDesiredSampleTimeAndDuration method [Media Foundation]","IMFDesiredSample interface","evr/IMFDesiredSample::SetDesiredSampleTimeAndDuration","mf.imfdesiredsample_setdesiredsampletimeandduration"]
old-location: mf\imfdesiredsample_setdesiredsampletimeandduration.htm
tech.root: mfarchive
ms.assetid: 12877b24-83ec-4156-b411-f07202fdfd62
ms.date: 12/05/2018
ms.keywords: 12877b24-83ec-4156-b411-f07202fdfd62, IMFDesiredSample interface [Media Foundation],SetDesiredSampleTimeAndDuration method, IMFDesiredSample.SetDesiredSampleTimeAndDuration, IMFDesiredSample::SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration, SetDesiredSampleTimeAndDuration method [Media Foundation], SetDesiredSampleTimeAndDuration method [Media Foundation],IMFDesiredSample interface, evr/IMFDesiredSample::SetDesiredSampleTimeAndDuration, mf.imfdesiredsample_setdesiredsampletimeandduration
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
 - IMFDesiredSample::SetDesiredSampleTimeAndDuration
 - evr/IMFDesiredSample::SetDesiredSampleTimeAndDuration
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
 - IMFDesiredSample.SetDesiredSampleTimeAndDuration
archived: true
---

# IMFDesiredSample::SetDesiredSampleTimeAndDuration


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Called by the presenter to set the time and duration of the sample that it requests from the mixer.

## -parameters

### -param hnsSampleTime [in]

The time of the requested sample.

### -param hnsSampleDuration [in]

The duration of the requested sample.

## -remarks

This value should be set prior to passing the buffer to the mixer for a Mix operation. The mixer sets the actual start and duration times on the sample before sending it back.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>