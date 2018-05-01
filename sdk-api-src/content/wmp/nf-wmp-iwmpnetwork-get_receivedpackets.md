---
UID: NF:wmp.IWMPNetwork.get_receivedPackets
title: IWMPNetwork::get_receivedPackets method
author: windows-driver-content
description: The get_receivedPackets method retrieves the number of packets received.
old-location: wmp\iwmpnetwork_get_receivedpackets.htm
old-project: WMP
ms.assetid: 9a896a67-ef0c-4fd7-b352-3c091bea1ad8
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], get_receivedPackets method, IWMPNetwork::get_receivedPackets, IWMPNetworkget_receivedPackets, get_receivedPackets method [Windows Media Player], get_receivedPackets method [Windows Media Player], IWMPNetwork interface, get_receivedPackets,IWMPNetwork.get_receivedPackets, wmp.iwmpnetwork_get_receivedpackets, wmp/IWMPNetwork::get_receivedPackets
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPNetwork.get_receivedPackets
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_receivedPackets method


## -description



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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

