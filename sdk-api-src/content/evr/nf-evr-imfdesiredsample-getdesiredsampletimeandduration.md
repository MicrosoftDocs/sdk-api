---
UID: NF:evr.IMFDesiredSample.GetDesiredSampleTimeAndDuration
title: IMFDesiredSample::GetDesiredSampleTimeAndDuration (evr.h)
description: Called by the mixer to get the time and duration of the sample requested by the presenter.
helpviewer_keywords: ["095202ed-0272-4bda-a268-6a407ef74a94","GetDesiredSampleTimeAndDuration","GetDesiredSampleTimeAndDuration method [Media Foundation]","GetDesiredSampleTimeAndDuration method [Media Foundation]","IMFDesiredSample interface","IMFDesiredSample interface [Media Foundation]","GetDesiredSampleTimeAndDuration method","IMFDesiredSample.GetDesiredSampleTimeAndDuration","IMFDesiredSample::GetDesiredSampleTimeAndDuration","evr/IMFDesiredSample::GetDesiredSampleTimeAndDuration","mf.imfdesiredsample_getdesiredsampletimeandduration"]
old-location: mf\imfdesiredsample_getdesiredsampletimeandduration.htm
tech.root: mfarchive
ms.assetid: 095202ed-0272-4bda-a268-6a407ef74a94
ms.date: 12/05/2018
ms.keywords: 095202ed-0272-4bda-a268-6a407ef74a94, GetDesiredSampleTimeAndDuration, GetDesiredSampleTimeAndDuration method [Media Foundation], GetDesiredSampleTimeAndDuration method [Media Foundation],IMFDesiredSample interface, IMFDesiredSample interface [Media Foundation],GetDesiredSampleTimeAndDuration method, IMFDesiredSample.GetDesiredSampleTimeAndDuration, IMFDesiredSample::GetDesiredSampleTimeAndDuration, evr/IMFDesiredSample::GetDesiredSampleTimeAndDuration, mf.imfdesiredsample_getdesiredsampletimeandduration
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
 - IMFDesiredSample::GetDesiredSampleTimeAndDuration
 - evr/IMFDesiredSample::GetDesiredSampleTimeAndDuration
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
 - IMFDesiredSample.GetDesiredSampleTimeAndDuration
archived: true
---

# IMFDesiredSample::GetDesiredSampleTimeAndDuration


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Called by the mixer to get the time and duration of the sample requested by the presenter.

## -parameters

### -param phnsSampleTime [out]

Receives the desired sample time that should be mixed.

### -param phnsSampleDuration [out]

Receives the sample duration that should be mixed.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No time stamp was set for this sample. See <a href="/windows/desktop/api/evr/nf-evr-imfdesiredsample-clear">IMFDesiredSample::Clear</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>