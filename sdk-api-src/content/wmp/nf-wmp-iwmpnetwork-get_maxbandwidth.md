---
UID: NF:wmp.IWMPNetwork.get_maxBandwidth
title: IWMPNetwork::get_maxBandwidth (wmp.h)
description: The get_maxBandwidth method retrieves the maximum allowed bandwidth.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_maxBandwidth method","IWMPNetwork.get_maxBandwidth","IWMPNetwork::get_maxBandwidth","IWMPNetworkget_maxBandwidth","get_maxBandwidth","get_maxBandwidth method [Windows Media Player]","get_maxBandwidth method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_maxbandwidth","wmp/IWMPNetwork::get_maxBandwidth"]
old-location: wmp\iwmpnetwork_get_maxbandwidth.htm
tech.root: WMP
ms.assetid: b3b1b845-7aa5-49d7-a9da-52dea06e51c4
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_maxBandwidth method, IWMPNetwork.get_maxBandwidth, IWMPNetwork::get_maxBandwidth, IWMPNetworkget_maxBandwidth, get_maxBandwidth, get_maxBandwidth method [Windows Media Player], get_maxBandwidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_maxbandwidth, wmp/IWMPNetwork::get_maxBandwidth
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
 - IWMPNetwork::get_maxBandwidth
 - wmp/IWMPNetwork::get_maxBandwidth
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
 - IWMPNetwork.get_maxBandwidth
---

# IWMPNetwork::get_maxBandwidth


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_maxBandwidth</b> method retrieves the maximum allowed bandwidth.

## -parameters

### -param lMaxBandwidth [out]

Pointer to a <b>long</b> containing the maximum bandwidth.

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

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-close">IWMPCore::close</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-put_maxbandwidth">IWMPNetwork::put_maxBandwidth</a>