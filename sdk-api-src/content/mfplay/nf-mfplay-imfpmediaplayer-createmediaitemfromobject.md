---
UID: NF:mfplay.IMFPMediaPlayer.CreateMediaItemFromObject
title: IMFPMediaPlayer::CreateMediaItemFromObject
author: windows-sdk-content
description: Creates a media item from an object.
old-location: mf\imfpmediaplayer_createmediaitemfromobject.htm
tech.root: MedFound
ms.assetid: d647df89-b874-448e-ae41-ee3bcb55521f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateMediaItemFromObject, CreateMediaItemFromObject method [Media Foundation], CreateMediaItemFromObject method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],CreateMediaItemFromObject method, IMFPMediaPlayer.CreateMediaItemFromObject, IMFPMediaPlayer::CreateMediaItemFromObject, mf.imfpmediaplayer_createmediaitemfromobject, mfplay/IMFPMediaPlayer::CreateMediaItemFromObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::CreateMediaItemFromObject


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Creates a media item from an object.


## -parameters




### -param pIUnknownObj [in]

A pointer to the object's <b>IUnknown</b> interface. See Remarks.


### -param fSync [in]

If <b>TRUE</b>, the method blocks until it completes. If <b>FALSE</b>, the method does not block and completes asynchronously.


### -param dwUserData [in]

Application-defined value to store in the media item. To retrieve this value from the media item, call <a href="https://msdn.microsoft.com/aa99ced1-c32b-4bf5-b29a-e16eceddfed1">IMFPMediaItem::GetUserData</a>.


### -param ppMediaItem [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> interface. The caller must release the interface. If <i>fSync</i> is <b>TRUE</b>, this parameter must be a valid pointer. If <i>bSync</i> is <b>FALSE</b>, this parameter must be <b>NULL</b>.


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
The object's <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



The <i>pIUnknownObj</i> parameter must specify one of the following:

<ul>
<li>A pointer to a media source. Media sources expose the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">IMFMediaSource::Shutdown</a> on the media source.</li>
<li>A pointer to a byte stream. Byte streams expose the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface. Internally, the method calls the <a href="https://msdn.microsoft.com/e4a4aad5-0924-4251-b0da-6919ae010bf0">IMFSourceResolver::CreateObjectFromByteStream</a> method to create a media source from the byte stream. Therefore, a byte-stream handler must be registered for the byte stream. For more information about byte-stream handlers, see <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>.

</li>
</ul>
This method does not queue the media item for playback. To queue the item for playback, call <a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">IMFPMediaPlayer::SetMediaItem</a>.

The <b>CreateMediaItemFromObject</b> method can be called either synchronously or asynchronously: 

<ul>
<li>If <i>fSync</i> is <b>TRUE</b>, the method completes synchronously. The <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> pointer is returned in the <i>ppMediaItem</i> parameter. </li>
<li>If <i>fSync</i> is <b>FALSE</b>, the method completes asynchronously. When the operation completes, the application's <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b>. The event data contains the <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> pointer for the new media item.</li>
</ul>
The callback interface is set when you first call <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a> to create the MFPlay player object. If you do not provide a callback interface, the <i>fSync</i> parameter must be <b>TRUE</b>. Otherwise, <b>CreateMediaItemFromObject</b> returns <b>MF_E_INVALIDREQUEST</b>. 

If you make multiple asynchronous calls to <b>CreateMediaItemFromObject</b>, they are not guaranteed to complete in the same order. Use the <i>dwUserData</i> parameter to match created media items with pending requests.

<h3><a id="Configuring_the_Source"></a><a id="configuring_the_source"></a><a id="CONFIGURING_THE_SOURCE"></a>Configuring the Source</h3>
If <i>pIUnknownObj</i> points to a byte stream, you can configure the media source by performing the following steps:

<ol>
<li>Call <b>QueryInterface</b> on the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> pointer to get the <b>IPropertyStore</b> interface.</li>
<li>Call <b>IPropertyStore::SetValue</b> to set properties for the media source. For a list of configuration properties, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>. Third-party media sources may define custom properties.</li>
<li>Call the <b>CreateMediaItemFromObject</b> method to create the media item.</li>
</ol>
If <i>pIUnknownObj</i> points to a media source, you can configure the source at the time that you create it.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

