---
UID: NF:wmp.IWMPNetwork.get_receivedPackets
title: IWMPNetwork::get_receivedPackets (wmp.h)
description: The get_receivedPackets method retrieves the number of packets received.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_receivedPackets method","IWMPNetwork.get_receivedPackets","IWMPNetwork::get_receivedPackets","IWMPNetworkget_receivedPackets","get_receivedPackets","get_receivedPackets method [Windows Media Player]","get_receivedPackets method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_receivedpackets","wmp/IWMPNetwork::get_receivedPackets"]
old-location: wmp\iwmpnetwork_get_receivedpackets.htm
tech.root: WMP
ms.assetid: 9a896a67-ef0c-4fd7-b352-3c091bea1ad8
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_receivedPackets method, IWMPNetwork.get_receivedPackets, IWMPNetwork::get_receivedPackets, IWMPNetworkget_receivedPackets, get_receivedPackets, get_receivedPackets method [Windows Media Player], get_receivedPackets method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_receivedpackets, wmp/IWMPNetwork::get_receivedPackets
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
 - IWMPNetwork::get_receivedPackets
 - wmp/IWMPNetwork::get_receivedPackets
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
 - IWMPNetwork.get_receivedPackets
---

# IWMPNetwork::get_receivedPackets


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_receivedPackets</b> method retrieves the number of packets received.

## -parameters

### -param plReceivedPackets [out]

Pointer to a <b>long</b> containing the received packets.

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

Each time playback is stopped and restarted, the value retrieved from this method is reset to zero. The value is not reset if playback is paused.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>