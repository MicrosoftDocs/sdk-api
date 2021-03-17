---
UID: NF:sensevts.ISensNetwork.ConnectionMadeNoQOCInfo
title: ISensNetwork::ConnectionMadeNoQOCInfo (sensevts.h)
description: The ConnectionMadeNoQOCInfo method notifies your application that the specified connection has been established with no Quality of Connection information available.
helpviewer_keywords: ["ConnectionMadeNoQOCInfo","ConnectionMadeNoQOCInfo method [SENS]","ConnectionMadeNoQOCInfo method [SENS]","ISensNetwork interface","ISensNetwork interface [SENS]","ConnectionMadeNoQOCInfo method","ISensNetwork.ConnectionMadeNoQOCInfo","ISensNetwork::ConnectionMadeNoQOCInfo","_zaw_isensnetwork_connectionmadenoqocinfo","sens.isensnetwork_connectionmadenoqocinfo","sensevts/ISensNetwork::ConnectionMadeNoQOCInfo","syncmgr.isensnetwork_connectionmadenoqocinfo"]
old-location: sens\isensnetwork_connectionmadenoqocinfo.htm
tech.root: Sens
ms.assetid: a27dd3c7-e3f6-4ccb-b23a-17b15235245c
ms.date: 12/05/2018
ms.keywords: ConnectionMadeNoQOCInfo, ConnectionMadeNoQOCInfo method [SENS], ConnectionMadeNoQOCInfo method [SENS],ISensNetwork interface, ISensNetwork interface [SENS],ConnectionMadeNoQOCInfo method, ISensNetwork.ConnectionMadeNoQOCInfo, ISensNetwork::ConnectionMadeNoQOCInfo, _zaw_isensnetwork_connectionmadenoqocinfo, sens.isensnetwork_connectionmadenoqocinfo, sensevts/ISensNetwork::ConnectionMadeNoQOCInfo, syncmgr.isensnetwork_connectionmadenoqocinfo
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
 - ISensNetwork::ConnectionMadeNoQOCInfo
 - sensevts/ISensNetwork::ConnectionMadeNoQOCInfo
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
 - ISensNetwork.ConnectionMadeNoQOCInfo
---

# ISensNetwork::ConnectionMadeNoQOCInfo


## -description

The 
<b>ConnectionMadeNoQOCInfo</b> method notifies your application that the specified connection has been established with no Quality of Connection information available.
<div class="alert"><b>Note</b>  This method is only available for TCP/IP connections.</div><div> </div>

## -parameters

### -param bstrConnection [in]

For WAN connections, the information passed is the connection name. For WAN connections, the connection name is the name of the phone book entry. For LAN connections, the information passed is "LAN connection".

### -param ulType [in]

Connection type. This value can be CONNECTION_LAN (0) or CONNECTION_WAN (1).

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

SENS calls this method to notify your application that the specified connection has been established when Quality of Connection information is not available.

Filtering can be performed on the publisher property <i>ulConnectionMadeTypeNoQOC</i> by setting it to either CONNECTION_LAN or CONNECTION_WAN or both. Use 
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a> to set the publisher property.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isensnetwork">ISensNetwork</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isensnetwork-connectionmade">ISensNetwork::ConnectionMade</a>