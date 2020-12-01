---
UID: NF:wmp.IWMPNetwork.put_bufferingTime
title: IWMPNetwork::put_bufferingTime (wmp.h)
description: The put_bufferingTime method specifies the amount of time in milliseconds allocated for buffering incoming data before playing begins.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","put_bufferingTime method","IWMPNetwork.put_bufferingTime","IWMPNetwork::put_bufferingTime","IWMPNetworkput_bufferingTime","put_bufferingTime","put_bufferingTime method [Windows Media Player]","put_bufferingTime method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_put_bufferingtime","wmp/IWMPNetwork::put_bufferingTime"]
old-location: wmp\iwmpnetwork_put_bufferingtime.htm
tech.root: WMP
ms.assetid: 9f25992f-e3a0-477b-b445-1f3fb7d9eae1
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],put_bufferingTime method, IWMPNetwork.put_bufferingTime, IWMPNetwork::put_bufferingTime, IWMPNetworkput_bufferingTime, put_bufferingTime, put_bufferingTime method [Windows Media Player], put_bufferingTime method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_put_bufferingtime, wmp/IWMPNetwork::put_bufferingTime
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
 - IWMPNetwork::put_bufferingTime
 - wmp/IWMPNetwork::put_bufferingTime
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
 - IWMPNetwork.put_bufferingTime
---

# IWMPNetwork::put_bufferingTime


## -description

The <b>put_bufferingTime</b> method specifies the amount of time in milliseconds allocated for buffering incoming data before playing begins.

## -parameters

### -param lBufferingTime [in]

<b>long</b> containing the buffering time, which ranges from zero to 60,000 with a default value of 5,000.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingtime">IWMPNetwork::get_bufferingTime</a>