---
UID: NF:contentpartner.IWMPContentPartner.Download
title: IWMPContentPartner::Download (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Download method initiates the download of a set of media items.
helpviewer_keywords: ["Download","Download method [Windows Media Player]","Download method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","Download method","IWMPContentPartner.Download","IWMPContentPartner::Download","IWMPContentPartnerDownload","contentpartner/IWMPContentPartner::Download","wmp.iwmpcontentpartner_download"]
old-location: wmp\iwmpcontentpartner_download.htm
tech.root: WMP
ms.assetid: 0fa3ed40-e155-4e42-b031-d6cb8f8b4ac4
ms.date: 4/26/2023
ms.keywords: Download, Download method [Windows Media Player], Download method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],Download method, IWMPContentPartner.Download, IWMPContentPartner::Download, IWMPContentPartnerDownload, contentpartner/IWMPContentPartner::Download, wmp.iwmpcontentpartner_download
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
 - IWMPContentPartner::Download
 - contentpartner/IWMPContentPartner::Download
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
 - IWMPContentPartner.Download
---

# IWMPContentPartner::Download


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Download</b> method initiates the download of a set of media items.

## -parameters

### -param pInfo [in]

Pointer to an <a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist">IWMPContentContainerList</a> interface that describes the content to download.

### -param cookie [in]

A cookie that represents the download request.

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

This method initiates the process of inspecting the container list passed in <i>pInfo</i> and then returns immediately. As the plug-in inspects the container list, it calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack">IWMPContentPartnerCallback::DownloadTrack</a> once for each track in the container list. For more information about the download procedure, see <a href="/windows/desktop/WMP/downloading-media-content">Downloading Media Content</a>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist">IWMPContentContainerList Interface</a>



<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete">IWMPContentPartner::DownloadTrackComplete</a>