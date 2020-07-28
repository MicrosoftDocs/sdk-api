---
UID: NF:contentpartner.IWMPContentPartner.DownloadTrackComplete
title: IWMPContentPartner::DownloadTrackComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["DownloadTrackComplete","DownloadTrackComplete method [Windows Media Player]","DownloadTrackComplete method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","DownloadTrackComplete method","IWMPContentPartner.DownloadTrackComplete","IWMPContentPartner::DownloadTrackComplete","IWMPContentPartnerDownloadTrackComplete","contentpartner/IWMPContentPartner::DownloadTrackComplete","wmp.iwmpcontentpartner_downloadtrackcomplete"]
old-location: wmp\iwmpcontentpartner_downloadtrackcomplete.htm
tech.root: WMP
ms.assetid: 9614e266-259c-411f-93cf-9be87c930b16
ms.date: 12/05/2018
ms.keywords: DownloadTrackComplete, DownloadTrackComplete method [Windows Media Player], DownloadTrackComplete method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],DownloadTrackComplete method, IWMPContentPartner.DownloadTrackComplete, IWMPContentPartner::DownloadTrackComplete, IWMPContentPartnerDownloadTrackComplete, contentpartner/IWMPContentPartner::DownloadTrackComplete, wmp.iwmpcontentpartner_downloadtrackcomplete
f1_keywords:
- contentpartner/IWMPContentPartner.DownloadTrackComplete
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- contentpartner.h
api_name:
- IWMPContentPartner.DownloadTrackComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartner::DownloadTrackComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>DownloadTrackComplete</b> method notifies the content partner plug-in that Windows Media Player has finished downloading a track or that the download attempt failed.




## -parameters




### -param hrResult [in]

<b>HRESULT</b> indicating success or failure of the download. Any success code indicates that the Player successfully downloaded the track. Any failure code indicates that the Player failed to download the track.


### -param contentID [in]

Content ID of the track in question.


### -param downloadTrackParam [in]

Parameter that the plug-in previously passed to <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack">IWMPContentPartnerCallback::DownloadTrack</a>. This parameter is meaningful only to the online store; it is not interpreted by Windows Media Player.


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



To learn how the Player and the plug-in work together to download a set of tracks, see <a href="https://docs.microsoft.com/windows/desktop/WMP/downloading-media-content">Downloading Media Content</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download">IWMPContentPartner::Download</a>
 

 

