---
UID: NF:mfplay.IMFPMediaItem.GetObject
title: IMFPMediaItem::GetObject (mfplay.h)
description: Gets the object that was used to create the media item.helpviewer_keywords: ["GetObject","GetObject method [Media Foundation]","GetObject method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetObject method","IMFPMediaItem.GetObject","IMFPMediaItem::GetObject","mf.imfpmediaitem_getobject","mfplay/IMFPMediaItem::GetObject"]
old-location: mf\imfpmediaitem_getobject.htm
tech.root: medfound
ms.assetid: 6a6abc57-149d-4e4b-a29f-7b712d24e6df
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Media Foundation], GetObject method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetObject method, IMFPMediaItem.GetObject, IMFPMediaItem::GetObject, mf.imfpmediaitem_getobject, mfplay/IMFPMediaItem::GetObject
f1_keywords:
- mfplay/IMFPMediaItem.GetObject
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
- IMFPMediaItem.GetObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetObject


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the object that was used to create the media item.


## -parameters




### -param ppIUnknown [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface.


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
<dt><b>MF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The media item was created from a URL, not from an object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">IMFPMediaPlayer::Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



The object pointer is set if the application uses <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create the media item. Otherwise, <b>GetObject</b> returns  MF_E_NOTFOUND.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

