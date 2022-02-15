---
UID: NF:mfidl.IMFMediaStream.RequestSample
title: IMFMediaStream::RequestSample (mfidl.h)
description: Requests a sample from the media source.
helpviewer_keywords: ["3838167b-5774-47f5-9b8d-2882eaa97167","IMFMediaStream interface [Media Foundation]","RequestSample method","IMFMediaStream.RequestSample","IMFMediaStream::RequestSample","RequestSample","RequestSample method [Media Foundation]","RequestSample method [Media Foundation]","IMFMediaStream interface","mf.imfmediastream_requestsample","mfidl/IMFMediaStream::RequestSample"]
old-location: mf\imfmediastream_requestsample.htm
tech.root: mf
ms.assetid: 3838167b-5774-47f5-9b8d-2882eaa97167
ms.date: 12/05/2018
ms.keywords: 3838167b-5774-47f5-9b8d-2882eaa97167, IMFMediaStream interface [Media Foundation],RequestSample method, IMFMediaStream.RequestSample, IMFMediaStream::RequestSample, RequestSample, RequestSample method [Media Foundation], RequestSample method [Media Foundation],IMFMediaStream interface, mf.imfmediastream_requestsample, mfidl/IMFMediaStream::RequestSample
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaStream::RequestSample
 - mfidl/IMFMediaStream::RequestSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaStream.RequestSample
---

# IMFMediaStream::RequestSample


## -description

Requests a sample from the media source.

## -parameters

### -param pToken [in]

Pointer to the <b>IUnknown</b> interface to an object that is used as a token for the request. The caller must implement this object. This parameter can be <b>NULL</b>. See Remarks.

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
<dt><b>MF_E_END_OF_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The end of the stream was reached.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MEDIA_SOURCE_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
The media source is stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.
              

</td>
</tr>
</table>

## -remarks

If <i>pToken</i> is not <b>NULL</b>, the media stream calls <b>AddRef</b> on <i>pToken</i> and places the token in a first-in, first-out queue.

When the next sample is available, the media stream stream does the following:

<ol>
<li>Pulls the first token from the queue.
          </li>
<li>Sets the <a href="/windows/desktop/medfound/mfsampleextension-token-attribute">MFSampleExtension_Token</a> attribute on the media sample. The attribute data is a pointer to the token object.
          </li>
<li>Sends an <a href="/windows/desktop/medfound/memediasample">MEMediaSample</a> event. The event data is a pointer to the media sample's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface.
          </li>
<li>Calls <b>Release</b> on the token.
          </li>
</ol>
If the media stream cannot fulfill the caller's request for a sample, it simply releases the token object and skips steps 2 and 3.

The caller should monitor the reference count on the request token. If the media stream sends an <a href="/windows/desktop/medfound/memediasample">MEMediaSample</a> event, get the <a href="/windows/desktop/medfound/mfsampleextension-token-attribute">MFSampleExtension_Token</a> attribute from the sample and match the attribute value against the token. If the token's reference count falls to zero and you did not receive an MEMediaSample event, it means that the request was dropped.

Because the Media Foundation pipeline is multithreaded, the source's <b>RequestSample</b> method might get called after the source has stopped. If the media source is stopped, the method should return <b>MF_E_MEDIA_SOURCE_WRONGSTATE</b>. The pipeline does not treat this return code as an error condition. If the source returns any other error code, the pipeline treats it as fatal error and halts the session.<div class="alert"><b>Note</b>  Earlier versions of the documentation listed the wrong error code for this case.</div>
<div> </div>


If the media source is paused, the method succeeds, but the stream does not deliver the sample until the source is started again.

If a media source encounters an error asynchronously while processing data, it should signal the error in one of the following ways (but not both):

<ul>
<li>Return an error code from the next <b>RequestSample</b> call.</li>
<li>Send an <a href="/windows/desktop/medfound/meerror">MEError</a> event.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream">IMFMediaStream</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>