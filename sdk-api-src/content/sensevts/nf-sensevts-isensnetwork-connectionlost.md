---
UID: NF:sensevts.ISensNetwork.ConnectionLost
title: ISensNetwork::ConnectionLost (sensevts.h)
description: The ConnectionLost method notifies your application that the specified connection has been dropped.
helpviewer_keywords: ["CONNECTION_LAN","CONNECTION_WAN","ConnectionLost","ConnectionLost method [SENS]","ConnectionLost method [SENS]","ISensNetwork interface","ISensNetwork interface [SENS]","ConnectionLost method","ISensNetwork.ConnectionLost","ISensNetwork::ConnectionLost","_zaw_isensnetwork_connectionlost","sens.isensnetwork_connectionlost","sensevts/ISensNetwork::ConnectionLost","syncmgr.isensnetwork_connectionlost"]
old-location: sens\isensnetwork_connectionlost.htm
tech.root: Sens
ms.assetid: b91e46b9-7931-4959-97de-fa882a56e406
ms.date: 12/05/2018
ms.keywords: CONNECTION_LAN, CONNECTION_WAN, ConnectionLost, ConnectionLost method [SENS], ConnectionLost method [SENS],ISensNetwork interface, ISensNetwork interface [SENS],ConnectionLost method, ISensNetwork.ConnectionLost, ISensNetwork::ConnectionLost, _zaw_isensnetwork_connectionlost, sens.isensnetwork_connectionlost, sensevts/ISensNetwork::ConnectionLost, syncmgr.isensnetwork_connectionlost
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
req.lib: 
req.dll: Sens.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensNetwork::ConnectionLost
 - sensevts/ISensNetwork::ConnectionLost
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensNetwork.ConnectionLost
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
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a> to set the publisher property.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isensnetwork">ISensNetwork</a>