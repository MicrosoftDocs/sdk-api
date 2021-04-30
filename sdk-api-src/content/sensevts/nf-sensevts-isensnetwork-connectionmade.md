---
UID: NF:sensevts.ISensNetwork.ConnectionMade
title: ISensNetwork::ConnectionMade (sensevts.h)
description: The ConnectionMade method notifies your application that the specified connection has been established.
helpviewer_keywords: ["ConnectionMade","ConnectionMade method [SENS]","ConnectionMade method [SENS]","ISensNetwork interface","ISensNetwork interface [SENS]","ConnectionMade method","ISensNetwork.ConnectionMade","ISensNetwork::ConnectionMade","_zaw_isensnetwork_connectionmade","sens.isensnetwork_connectionmade","sensevts/ISensNetwork::ConnectionMade","syncmgr.isensnetwork_connectionmade"]
old-location: sens\isensnetwork_connectionmade.htm
tech.root: Sens
ms.assetid: 3b067a6f-ba4c-4914-aa5b-e0fd7690e75c
ms.date: 12/05/2018
ms.keywords: ConnectionMade, ConnectionMade method [SENS], ConnectionMade method [SENS],ISensNetwork interface, ISensNetwork interface [SENS],ConnectionMade method, ISensNetwork.ConnectionMade, ISensNetwork::ConnectionMade, _zaw_isensnetwork_connectionmade, sens.isensnetwork_connectionmade, sensevts/ISensNetwork::ConnectionMade, syncmgr.isensnetwork_connectionmade
req.header: sensevts.h
req.include-header: 
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
 - ISensNetwork::ConnectionMade
 - sensevts/ISensNetwork::ConnectionMade
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
 - ISensNetwork.ConnectionMade
---

# ISensNetwork::ConnectionMade


## -description

The 
<b>ConnectionMade</b> method notifies your application that the specified connection has been established.
<div class="alert"><b>Note</b>  This method is only available for TCP/IP connections.</div><div> </div>

## -parameters

### -param bstrConnection [in]

For WAN connections, the information passed is the connection name. For WAN connections, the connection name is the name of the phone book entry. For LAN connections, the information passed is "LAN connection".

### -param ulType [in]

Connection type. This value can be CONNECTION_LAN (0) or CONNECTION_WAN (1).

### -param lpQOCInfo [in]

Pointer to the 
<a href="/windows/desktop/api/sensevts/ns-sensevts-sens_qocinfo">SENS_QOCINFO</a> structure which contains Quality of Connection information.

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

SENS calls this method to notify your application that the specified connection has been established. SENS also provides a pointer to a structure containing Quality of Connection information.

Filtering can be performed on the publisher property <i>ulConnectionMadeType</i> by setting it to either CONNECTION_LAN or CONNECTION_WAN or both. Use 
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a> to set the publisher property.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isensnetwork">ISensNetwork</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmadenoqocinfo">ISensNetwork::ConnectionMadeNoQOCInfo</a>



<a href="/windows/desktop/api/sensevts/ns-sensevts-sens_qocinfo">SENS_QOCINFO</a>