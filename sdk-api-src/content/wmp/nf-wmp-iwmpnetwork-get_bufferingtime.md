---
UID: NF:wmp.IWMPNetwork.get_bufferingTime
title: IWMPNetwork::get_bufferingTime (wmp.h)
description: The get_bufferingTime method retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_bufferingTime method","IWMPNetwork.get_bufferingTime","IWMPNetwork::get_bufferingTime","IWMPNetworkget_bufferingTime","get_bufferingTime","get_bufferingTime method [Windows Media Player]","get_bufferingTime method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_bufferingtime","wmp/IWMPNetwork::get_bufferingTime"]
old-location: wmp\iwmpnetwork_get_bufferingtime.htm
tech.root: WMP
ms.assetid: a42a7187-9bf2-4db5-8176-6912e18c4d50
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bufferingTime method, IWMPNetwork.get_bufferingTime, IWMPNetwork::get_bufferingTime, IWMPNetworkget_bufferingTime, get_bufferingTime, get_bufferingTime method [Windows Media Player], get_bufferingTime method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bufferingtime, wmp/IWMPNetwork::get_bufferingTime
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
 - IWMPNetwork::get_bufferingTime
 - wmp/IWMPNetwork::get_bufferingTime
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
 - IWMPNetwork.get_bufferingTime
---

# IWMPNetwork::get_bufferingTime


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_bufferingTime</b> method retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.

## -parameters

### -param plBufferingTime [out]

Pointer to a <b>long</b> containing the buffering time, which ranges from zero to 60,000 with a default value of 5,000.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-put_bufferingtime">IWMPNetwork::put_bufferingTime</a>