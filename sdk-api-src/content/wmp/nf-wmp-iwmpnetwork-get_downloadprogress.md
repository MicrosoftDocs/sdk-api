---
UID: NF:wmp.IWMPNetwork.get_downloadProgress
title: IWMPNetwork::get_downloadProgress (wmp.h)
description: The get_downloadProgress method retrieves the percentage of the download completed.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_downloadProgress method","IWMPNetwork.get_downloadProgress","IWMPNetwork::get_downloadProgress","IWMPNetworkget_downloadProgress","get_downloadProgress","get_downloadProgress method [Windows Media Player]","get_downloadProgress method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_downloadprogress","wmp/IWMPNetwork::get_downloadProgress"]
old-location: wmp\iwmpnetwork_get_downloadprogress.htm
tech.root: WMP
ms.assetid: e9ed2027-cba4-4701-a416-a2190b51570c
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_downloadProgress method, IWMPNetwork.get_downloadProgress, IWMPNetwork::get_downloadProgress, IWMPNetworkget_downloadProgress, get_downloadProgress, get_downloadProgress method [Windows Media Player], get_downloadProgress method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_downloadprogress, wmp/IWMPNetwork::get_downloadProgress
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPNetwork::get_downloadProgress
 - wmp/IWMPNetwork::get_downloadProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPNetwork.get_downloadProgress
---

# IWMPNetwork::get_downloadProgress


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_downloadProgress</b> method retrieves the percentage of the download completed.

## -parameters

### -param plDownloadProgress [out]

Pointer to a <b>long</b> containing the download progress.

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

When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the <b>get_downloadProgress</b> method retrieves the percentage of the total file that has been downloaded. This feature is currently supported only for digital media files downloaded from web servers. The following file formats can be downloaded and played simultaneously:

<ul>
<li>Advanced Systems Format (ASF)</li>
<li>Windows Media Audio (WMA)</li>
<li>Windows Media Video (WMV)</li>
<li>MP3</li>
<li>MPEG</li>
<li>WAV</li>
</ul>
In addition, some AVI files can be downloaded and played simultaneously.

Use the <b>IWMPEvents::Buffering</b> event to determine when buffering starts or stops.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-buffering">IWMPEvents::Buffering</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>