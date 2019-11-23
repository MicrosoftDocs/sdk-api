---
UID: NF:wmp.IWMPNetwork.get_lostPackets
title: IWMPNetwork::get_lostPackets (wmp.h)

description: The get_lostPackets method retrieves the number of packets lost.
old-location: wmp\iwmpnetwork_get_lostpackets.htm
tech.root: WMP
ms.assetid: 821b9bfc-931c-4e83-a899-4755bad3e7ae

ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_lostPackets method, IWMPNetwork.get_lostPackets, IWMPNetwork::get_lostPackets, IWMPNetworkget_lostPackets, get_lostPackets, get_lostPackets method [Windows Media Player], get_lostPackets method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_lostpackets, wmp/IWMPNetwork::get_lostPackets
ms.topic: method
f1_keywords: 
 - "wmp/IWMPNetwork.get_lostPackets"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPNetwork.get_lostPackets
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork::get_lostPackets


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>
 

 

