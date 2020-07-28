---
UID: NF:mfplay.IMFPMediaPlayer.CreateMediaItemFromObject
title: IMFPMediaPlayer::CreateMediaItemFromObject (mfplay.h)
description: Creates a media item from an object.
helpviewer_keywords: ["CreateMediaItemFromObject","CreateMediaItemFromObject method [Media Foundation]","CreateMediaItemFromObject method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","CreateMediaItemFromObject method","IMFPMediaPlayer.CreateMediaItemFromObject","IMFPMediaPlayer::CreateMediaItemFromObject","mf.imfpmediaplayer_createmediaitemfromobject","mfplay/IMFPMediaPlayer::CreateMediaItemFromObject"]
old-location: mf\imfpmediaplayer_createmediaitemfromobject.htm
tech.root: mf
ms.assetid: d647df89-b874-448e-ae41-ee3bcb55521f
ms.date: 12/05/2018
ms.keywords: CreateMediaItemFromObject, CreateMediaItemFromObject method [Media Foundation], CreateMediaItemFromObject method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],CreateMediaItemFromObject method, IMFPMediaPlayer.CreateMediaItemFromObject, IMFPMediaPlayer::CreateMediaItemFromObject, mf.imfpmediaplayer_createmediaitemfromobject, mfplay/IMFPMediaPlayer::CreateMediaItemFromObject
f1_keywords:
- mfplay/IMFPMediaPlayer.CreateMediaItemFromObject
dev_langs:
- c++
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplay.h
api_name:
- IMFPMediaPlayer.CreateMediaItemFromObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::CreateMediaItemFromObject


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Creates a media item from an object.


## -parameters




### -param pIUnknownObj [in]

A pointer to the object's <b>IUnknown</b> interface. See Remarks.


### -param fSync [in]

If <b>TRUE</b>, the method blocks until it completes. If <b>FALSE</b>, the method does not block and completes asynchronously.


### -param dwUserData [in]

Application-defined value to store in the media item. To retrieve this value from the media item, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata">IMFPMediaItem::GetUserData</a>.


### -param ppMediaItem [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface. The caller must release the interface. If <i>fSync</i> is <b>TRUE</b>, this parameter must be a valid pointer. If <i>bSync</i> is <b>FALSE</b>, this parameter must be <b>NULL</b>.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid request. This error can occur when <i>fSync</i> is <b>FALSE</b> and the application did not provide a callback interface. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



The <i>pIUnknownObj</i> parameter must specify one of the following:

<ul>
<li>A pointer to a media source. Media sources expose the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface. It is the caller's responsibility to call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">IMFMediaSource::Shutdown</a> on the media source.</li>
<li>A pointer to a byte stream. Byte streams expose the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface. Internally, the method calls the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream">IMFSourceResolver::CreateObjectFromByteStream</a> method to create a media source from the byte stream. Therefore, a byte-stream handler must be registered for the byte stream. For more information about byte-stream handlers, see <a href="https://docs.microsoft.com/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>.

</li>
</ul>
This method does not queue the media item for playback. To queue the item for playback, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a>.

The <b>CreateMediaItemFromObject</b> method can be called either synchronously or asynchronously: 

<ul>
<li>If <i>fSync</i> is <b>TRUE</b>, the method completes synchronously. The <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> pointer is returned in the <i>ppMediaItem</i> parameter. </li>
<li>If <i>fSync</i> is <b>FALSE</b>, the method completes asynchronously. When the operation completes, the application's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b>. The event data contains the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> pointer for the new media item.</li>
</ul>
The callback interface is set when you first call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a> to create the MFPlay player object. If you do not provide a callback interface, the <i>fSync</i> parameter must be <b>TRUE</b>. Otherwise, <b>CreateMediaItemFromObject</b> returns <b>MF_E_INVALIDREQUEST</b>. 

If you make multiple asynchronous calls to <b>CreateMediaItemFromObject</b>, they are not guaranteed to complete in the same order. Use the <i>dwUserData</i> parameter to match created media items with pending requests.

<h3><a id="Configuring_the_Source"></a><a id="configuring_the_source"></a><a id="CONFIGURING_THE_SOURCE"></a>Configuring the Source</h3>
If <i>pIUnknownObj</i> points to a byte stream, you can configure the media source by performing the following steps:

<ol>
<li>Call <b>QueryInterface</b> on the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> pointer to get the <b>IPropertyStore</b> interface.</li>
<li>Call <b>IPropertyStore::SetValue</b> to set properties for the media source. For a list of configuration properties, see <a href="https://docs.microsoft.com/windows/desktop/medfound/configuring-a-media-source">Configuring a Media Source</a>. Third-party media sources may define custom properties.</li>
<li>Call the <b>CreateMediaItemFromObject</b> method to create the media item.</li>
</ol>
If <i>pIUnknownObj</i> points to a media source, you can configure the source at the time that you create it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

