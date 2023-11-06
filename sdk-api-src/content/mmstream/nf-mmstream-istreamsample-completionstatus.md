---
UID: NF:mmstream.IStreamSample.CompletionStatus
title: IStreamSample::CompletionStatus (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the status of the current sample's latest asynchronous update. If the update isn't complete, you can force it to complete.
helpviewer_keywords: ["CompletionStatus","CompletionStatus method [DirectShow]","CompletionStatus method [DirectShow]","IStreamSample interface","IStreamSample interface [DirectShow]","CompletionStatus method","IStreamSample.CompletionStatus","IStreamSample::CompletionStatus","IStreamSampleCompletionStatus","dshow.istreamsample_completionstatus","mmstream/IStreamSample::CompletionStatus"]
old-location: dshow\istreamsample_completionstatus.htm
tech.root: dshow
ms.assetid: bfc3fd16-20b1-4581-abb0-66781aa3d584
ms.date: 4/26/2023
ms.keywords: CompletionStatus, CompletionStatus method [DirectShow], CompletionStatus method [DirectShow],IStreamSample interface, IStreamSample interface [DirectShow],CompletionStatus method, IStreamSample.CompletionStatus, IStreamSample::CompletionStatus, IStreamSampleCompletionStatus, dshow.istreamsample_completionstatus, mmstream/IStreamSample::CompletionStatus
req.header: mmstream.h
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
 - IStreamSample::CompletionStatus
 - mmstream/IStreamSample::CompletionStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IStreamSample.CompletionStatus
---

# IStreamSample::CompletionStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the status of the current sample's latest asynchronous update. If the update isn't complete, you can force it to complete.

## -parameters

### -param dwFlags [in]

Value that specifies whether to forcibly complete the update. This value is a combination of one or more of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>COMPSTAT_NOUPDATEOK (0x01)</td>
<td>Force the update to complete as soon as possible, even if the sample update isn't yet complete. If the sample is updating and you didn't set the COMPSTAT_WAIT flag, the method returns MS_S_PENDING. If the sample is waiting to be updated, this method removes it from the queue and returns MS_S_NOTUPDATED.</td>
</tr>
<tr>
<td>COMPSTAT_WAIT (0x02)</td>
<td>Wait until the sample finishes updating before returning from this method.</td>
</tr>
<tr>
<td>COMPSTAT_ABORT (0x04)</td>
<td>Forces the update to complete, even if it's currently updating. This leaves the sample data in an undefined state. Combine this value with the COMPSTAT_WAITFORCOMPLETION flag to ensure that the update canceled.</td>
</tr>
</table>

### -param dwMilliseconds [in]

If the <i>dwFlags</i> parameter is COMPSTAT_WAIT, this value is the number of milliseconds to wait for the update to complete. Specify INFINITE to indicate that you want to wait until the sample updates before this call returns.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The update aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_ENDOFSTREAM</b></dt>
</dl>
</td>
<td width="60%">
The sample wasn't updated because it reached the end of the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_NOUPDATE</b></dt>
</dl>
</td>
<td width="60%">
The update was forcibly completed; the sample was not updated by the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
An asynchronous update is pending.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample Interface</a>