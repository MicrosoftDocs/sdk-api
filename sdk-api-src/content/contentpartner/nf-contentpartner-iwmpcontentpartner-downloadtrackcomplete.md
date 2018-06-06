---
UID: NF:contentpartner.IWMPContentPartner.DownloadTrackComplete
title: IWMPContentPartner::DownloadTrackComplete
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_downloadtrackcomplete.htm
old-project: WMP
ms.assetid: 9614e266-259c-411f-93cf-9be87c930b16
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: DownloadTrackComplete, DownloadTrackComplete method [Windows Media Player], DownloadTrackComplete method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],DownloadTrackComplete method, IWMPContentPartner.DownloadTrackComplete, IWMPContentPartner::DownloadTrackComplete, IWMPContentPartnerDownloadTrackComplete, contentpartner/IWMPContentPartner::DownloadTrackComplete, wmp.iwmpcontentpartner_downloadtrackcomplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.DownloadTrackComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

Parameter that the plug-in previously passed to <a href="https://msdn.microsoft.com/fe8772fa-2eb4-4dfe-b677-e667b6021690">IWMPContentPartnerCallback::DownloadTrack</a>. This parameter is meaningful only to the online store; it is not interpreted by Windows Media Player.


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



To learn how the Player and the plug-in work together to download a set of tracks, see <a href="https://msdn.microsoft.com/0a057e13-6e0c-4a8f-9cab-051183e6b222">Downloading Media Content</a>.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/0fa3ed40-e155-4e42-b031-d6cb8f8b4ac4">IWMPContentPartner::Download</a>
 

 

