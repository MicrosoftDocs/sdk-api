---
UID: NF:contentpartner.IWMPContentPartnerCallback.DownloadTrack
title: IWMPContentPartnerCallback::DownloadTrack (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["DownloadTrack","DownloadTrack method [Windows Media Player]","DownloadTrack method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","DownloadTrack method","IWMPContentPartnerCallback.DownloadTrack","IWMPContentPartnerCallback::DownloadTrack","IWMPContentPartnerCallbackDownloadTrack","contentpartner/IWMPContentPartnerCallback::DownloadTrack","wmp.iwmpcontentpartnercallback_downloadtrack"]
old-location: wmp\iwmpcontentpartnercallback_downloadtrack.htm
tech.root: WMP
ms.assetid: fe8772fa-2eb4-4dfe-b677-e667b6021690
ms.date: 4/26/2023
ms.keywords: DownloadTrack, DownloadTrack method [Windows Media Player], DownloadTrack method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],DownloadTrack method, IWMPContentPartnerCallback.DownloadTrack, IWMPContentPartnerCallback::DownloadTrack, IWMPContentPartnerCallbackDownloadTrack, contentpartner/IWMPContentPartnerCallback::DownloadTrack, wmp.iwmpcontentpartnercallback_downloadtrack
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
 - IWMPContentPartnerCallback::DownloadTrack
 - contentpartner/IWMPContentPartnerCallback::DownloadTrack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartnerCallback.DownloadTrack
---

# IWMPContentPartnerCallback::DownloadTrack


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>DownloadTrack</b> method instructs Windows Media Player to download or not to download a particular media item.

## -parameters

### -param cookie [in]

A cookie that identifies a download session. Windows Media Player previously supplied this cookie to the content partner plug-in by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download">IWMPContentPartner::Download</a>.

### -param bstrTrackURL [in]

The URL of the track to download.

### -param dwServiceTrackID [in]

The ID of the track in question.

### -param bstrDownloadParams [in]

Data that the online store wants to associate with the track in question. Windows Media Player does not interpret this data; it is meaningful only to the online store. Windows Media player passes this data back to the online store when it calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete">IWMPContentPartner::DownloadTrackComplete</a>.

### -param hrDownload [in]

An <b>HRESULT</b> that specifies whether to download the track. Any success code specifies that the Player should download the track. Any failure code specifies that the Player should not download the track.

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
</table>

## -remarks

For an explanation of how the Player and the plug-in work together to download a set of tracks, see <a href="/windows/desktop/WMP/downloading-media-content">Downloading Media Content</a>.

This method must be called only after a license has been predelivered for the file. The file will be placed in the user's Music folder and automatically added to the library when downloading is complete.

## -see-also

<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download">IWMPContentPartner::Download</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete">IWMPContentPartner::DownloadTrackComplete</a>



<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>