---
UID: NF:wmp.IWMPNetwork.get_sourceProtocol
title: IWMPNetwork::get_sourceProtocol method
author: windows-driver-content
description: The get_sourceProtocol method retrieves the source protocol used to receive data.
old-location: wmp\iwmpnetwork_get_sourceprotocol.htm
old-project: WMP
ms.assetid: 6703ce88-9ca8-4401-b297-f765c4b15b84
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], get_sourceProtocol method, IWMPNetwork::get_sourceProtocol, IWMPNetworkget_sourceProtocol, get_sourceProtocol method [Windows Media Player], get_sourceProtocol method [Windows Media Player], IWMPNetwork interface, get_sourceProtocol,IWMPNetwork.get_sourceProtocol, wmp.iwmpnetwork_get_sourceprotocol, wmp/IWMPNetwork::get_sourceProtocol
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
-	IWMPNetwork.get_sourceProtocol
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_sourceProtocol method


## -description



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




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

