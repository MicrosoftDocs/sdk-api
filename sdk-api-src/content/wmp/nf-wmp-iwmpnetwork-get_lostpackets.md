---
UID: NF:wmp.IWMPNetwork.get_lostPackets
title: IWMPNetwork::get_lostPackets (wmp.h)
description: The get_lostPackets method retrieves the number of packets lost.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_lostPackets method","IWMPNetwork.get_lostPackets","IWMPNetwork::get_lostPackets","IWMPNetworkget_lostPackets","get_lostPackets","get_lostPackets method [Windows Media Player]","get_lostPackets method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_lostpackets","wmp/IWMPNetwork::get_lostPackets"]
old-location: wmp\iwmpnetwork_get_lostpackets.htm
tech.root: WMP
ms.assetid: 821b9bfc-931c-4e83-a899-4755bad3e7ae
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_lostPackets method, IWMPNetwork.get_lostPackets, IWMPNetwork::get_lostPackets, IWMPNetworkget_lostPackets, get_lostPackets, get_lostPackets method [Windows Media Player], get_lostPackets method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_lostpackets, wmp/IWMPNetwork::get_lostPackets
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
 - IWMPNetwork::get_lostPackets
 - wmp/IWMPNetwork::get_lostPackets
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
 - IWMPNetwork.get_lostPackets
---

# IWMPNetwork::get_lostPackets


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_lostPackets</b> method retrieves the number of packets lost.

## -parameters

### -param plLostPackets [out]

Pointer to a <b>long</b> containing the lost packets.

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

This method retrieves streaming media packets only, and will equal zero when using the HTTP protocol, which is lossless.

Packets may be lost for a number of reasons, such as the type and quality of the network connection.

Each time playback is stopped and restarted, the value retrieved from this method is reset to zero. The value is not reset if playback is paused. This method retrieves valid information only during run time when the URL for playback is set by using the <b>IWMPCore::put_URL</b> method.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>