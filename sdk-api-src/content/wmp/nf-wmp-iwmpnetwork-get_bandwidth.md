---
UID: NF:wmp.IWMPNetwork.get_bandWidth
title: IWMPNetwork::get_bandWidth (wmp.h)
description: The get_bandWidth method retrieves the current bandwidth of the media item.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_bandWidth method","IWMPNetwork.get_bandWidth","IWMPNetwork::get_bandWidth","IWMPNetworkget_bandWidth","get_bandWidth","get_bandWidth method [Windows Media Player]","get_bandWidth method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_bandwidth","wmp/IWMPNetwork::get_bandWidth"]
old-location: wmp\iwmpnetwork_get_bandwidth.htm
tech.root: WMP
ms.assetid: 910356d8-3d43-4516-ad30-b0ed288e5098
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bandWidth method, IWMPNetwork.get_bandWidth, IWMPNetwork::get_bandWidth, IWMPNetworkget_bandWidth, get_bandWidth, get_bandWidth method [Windows Media Player], get_bandWidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bandwidth, wmp/IWMPNetwork::get_bandWidth
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
 - IWMPNetwork::get_bandWidth
 - wmp/IWMPNetwork::get_bandWidth
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
 - IWMPNetwork.get_bandWidth
---

# IWMPNetwork::get_bandWidth


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_bandWidth</b> method retrieves the current bandwidth of the media item.

## -parameters

### -param plBandwidth [out]

Pointer to a <b>long</b> containing the bandwidth.

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

The value retrieved through <b>IWMPCore::put_URL</b> will be zero if the URL is not set. This method is only valid for streaming media.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>