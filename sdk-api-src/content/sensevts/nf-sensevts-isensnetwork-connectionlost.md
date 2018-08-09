---
UID: NF:sensevts.ISensNetwork.ConnectionLost
title: ISensNetwork::ConnectionLost
author: windows-sdk-content
description: The ConnectionLost method notifies your application that the specified connection has been dropped.
old-location: sens\isensnetwork_connectionlost.htm
old-project: sens
ms.assetid: b91e46b9-7931-4959-97de-fa882a56e406
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CONNECTION_LAN, CONNECTION_WAN, ConnectionLost, ConnectionLost method [SENS], ConnectionLost method [SENS],ISensNetwork interface, ISensNetwork interface [SENS],ConnectionLost method, ISensNetwork.ConnectionLost, ISensNetwork::ConnectionLost, _zaw_isensnetwork_connectionlost, sens.isensnetwork_connectionlost, sensevts/ISensNetwork::ConnectionLost, syncmgr.isensnetwork_connectionlost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensevts.h
req.include-header: Sensevts.h, Sens.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
tech.root: 
req.typenames: QOCINFO, *LPQOCINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensNetwork.ConnectionLost
product: Windows
targetos: Windows
req.lib: 
req.dll: Sens.dll
req.irql: 
req.product: ADAM
---

# ISensNetwork::ConnectionLost


## -description


The 
<b>ConnectionLost</b> method notifies your application that the specified connection has been dropped.
<div class="alert"><b>Note</b>  This method is only available for TCP/IP connections.</div><div> </div>

## -parameters




### -param bstrConnection [in]

For WAN connections, the information passed is the connection name. For WAN connections, the connection name is the name of the phone book entry. For LAN connections, the information passed is "LAN connection".


### -param ulType [in]

Connection type. This value can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONNECTION_LAN"></a><a id="connection_lan"></a><dl>
<dt><b>CONNECTION_LAN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The connection is to a Local Area Network (LAN).

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECTION_WAN"></a><a id="connection_wan"></a><dl>
<dt><b>CONNECTION_WAN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The connection is to a Wide Area Network (WAN).

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

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
Method returned successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify your application that the specified connection has been dropped.
			

Filtering can be performed on the publisher property <i>ulConnectionLostType</i> by setting it to either CONNECTION_LAN or CONNECTION_WAN or both. Use 
<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a> to set the publisher property.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="_cos_ieventsubscription">IEventSubscription</a>



<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/1cea5dff-13ea-4afb-84ac-7b8df4f55fc8">ISensNetwork</a>
 

 

