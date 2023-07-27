---
UID: NF:mmstream.IStreamSample.Update
title: IStreamSample::Update (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Performs a synchronous or an asynchronous update on the current sample.
helpviewer_keywords: ["IStreamSample interface [DirectShow]","Update method","IStreamSample.Update","IStreamSample::Update","IStreamSampleUpdate","Update","Update method [DirectShow]","Update method [DirectShow]","IStreamSample interface","dshow.istreamsample_update","mmstream/IStreamSample::Update"]
old-location: dshow\istreamsample_update.htm
tech.root: dshow
ms.assetid: 5f56e3f9-443b-4d67-bfed-3210e691ad4b
ms.date: 4/26/2023
ms.keywords: IStreamSample interface [DirectShow],Update method, IStreamSample.Update, IStreamSample::Update, IStreamSampleUpdate, Update, Update method [DirectShow], Update method [DirectShow],IStreamSample interface, dshow.istreamsample_update, mmstream/IStreamSample::Update
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
 - IStreamSample::Update
 - mmstream/IStreamSample::Update
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
 - IStreamSample.Update
---

# IStreamSample::Update


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Performs a synchronous or an asynchronous update on the current sample.

## -parameters

### -param dwFlags [in]

Flag that specifies whether the update is synchronous or asynchronous. The SSUPDATE_ASYNC flag specifies an asynchronous update, which you can set if both <i>hEvent</i> and <i>pfnAPC</i> are <b>NULL</b>. Use SSUPDATE_CONTINUOUS to continuously update the sample until you call the <a href="/windows/desktop/api/mmstream/nf-mmstream-istreamsample-completionstatus">IStreamSample::CompletionStatus</a> method.

### -param hEvent [in]

Handle to an event that this method will trigger when the update is complete.

### -param pfnAPC [in]

Pointer to a Win32 asynchronous procedure call (APC) function that this method will call after it completes the sample update.

### -param dwAPCData [in]

Value that this method passes to the function specified by the <i>pfnAPC</i> parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
This sample already has a pending update.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_ENDOFSTREAM</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the stream; the sample wasn't updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous update is pending.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate a sample because the allocator is not committed.

</td>
</tr>
</table>

## -remarks

This method can be used to perform a synchronous or asynchronous update of a sample. If both <i>hEvent</i> and <i>pfnAPC</i> are <b>NULL</b> then the update will be synchronous unless either of the SSUPDATE_ASYNC or SSUPDATE_CONTINUOUS flags is specified. When a synchronous update returns, the result of the function contains the I/O completion status.

You can't specify values for both <i>hEvent</i> and <i>pfnAPC</i>; the method will fail.

Asynchronous updates might complete before the update returns; in that case, the return value is S_OK. If you specify an event and the update returns S_OK, this method sets the event on return. If you specify an APC function and the update returns S_OK, the APC will not be queued and the function will not be called.

Asynchronous updates that don't complete prior to returning will return a value of MS_S_PENDING.

If an application creates multiple streams, it must perform an asynchronous update on each stream. Call <b>WaitForMultipleObjects</b> to wait for each stream update to complete, before making the next update. Otherwise, the application might block.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample Interface</a>