---
UID: NF:wmp.IWMPNetwork.get_sourceProtocol
title: IWMPNetwork::get_sourceProtocol (wmp.h)
description: The get_sourceProtocol method retrieves the source protocol used to receive data.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_sourceProtocol method","IWMPNetwork.get_sourceProtocol","IWMPNetwork::get_sourceProtocol","IWMPNetworkget_sourceProtocol","get_sourceProtocol","get_sourceProtocol method [Windows Media Player]","get_sourceProtocol method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_sourceprotocol","wmp/IWMPNetwork::get_sourceProtocol"]
old-location: wmp\iwmpnetwork_get_sourceprotocol.htm
tech.root: WMP
ms.assetid: 6703ce88-9ca8-4401-b297-f765c4b15b84
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_sourceProtocol method, IWMPNetwork.get_sourceProtocol, IWMPNetwork::get_sourceProtocol, IWMPNetworkget_sourceProtocol, get_sourceProtocol, get_sourceProtocol method [Windows Media Player], get_sourceProtocol method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_sourceprotocol, wmp/IWMPNetwork::get_sourceProtocol
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
 - IWMPNetwork::get_sourceProtocol
 - wmp/IWMPNetwork::get_sourceProtocol
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
 - IWMPNetwork.get_sourceProtocol
---

# IWMPNetwork::get_sourceProtocol


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_sourceProtocol</b> method retrieves the source protocol used to receive data.

## -parameters

### -param pbstrSourceProtocol [out]

Pointer to a <b>BSTR</b> containing the source protocol.

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

This method retrieves an empty string ("") when playing a CD or DVD.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>