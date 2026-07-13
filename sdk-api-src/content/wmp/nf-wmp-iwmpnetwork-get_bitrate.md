---
UID: NF:wmp.IWMPNetwork.get_bitRate
title: IWMPNetwork::get_bitRate (wmp.h)
description: The get_bitRate method retrieves the current bit rate being received.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_bitRate method","IWMPNetwork.get_bitRate","IWMPNetwork::get_bitRate","IWMPNetworkget_bitRate","get_bitRate","get_bitRate method [Windows Media Player]","get_bitRate method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_bitrate","wmp/IWMPNetwork::get_bitRate"]
old-location: wmp\iwmpnetwork_get_bitrate.htm
tech.root: WMP
ms.assetid: dfac8b29-47d9-4cee-801b-f43fa2bba6ed
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bitRate method, IWMPNetwork.get_bitRate, IWMPNetwork::get_bitRate, IWMPNetworkget_bitRate, get_bitRate, get_bitRate method [Windows Media Player], get_bitRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bitrate, wmp/IWMPNetwork::get_bitRate
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
 - IWMPNetwork::get_bitRate
 - wmp/IWMPNetwork::get_bitRate
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
 - IWMPNetwork.get_bitRate
---

# IWMPNetwork::get_bitRate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_bitRate</b> method retrieves the current bit rate being received.

## -parameters

### -param plBitRate [out]

Pointer to a <b>long</b> containing the bit rate.

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

The value retrieved by this method is a combination of the bit rates of both video and audio streams.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>