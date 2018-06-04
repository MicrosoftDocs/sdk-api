---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _RADIUSSERVERPROPERTIES enumeration


## -description


The values of the 
<b>RADIUSSERVERPROPERTIES</b> enumeration type enumerate the properties of the RADIUS server, that is the SDO computer.


## -enum-fields




### -field PROPERTY_RADIUSSERVER_AUTH_PORT

Comma separated list of the UDP ports over which RADIUS authentication packets are sent and received.


### -field PROPERTY_RADIUSSERVER_AUTH_SECRET

The shared secret for authentication.


### -field PROPERTY_RADIUSSERVER_ACCT_PORT

Comma separated list of the UDP ports over which RADIUS authentication packets are sent and received.


### -field PROPERTY_RADIUSSERVER_ACCT_SECRET

The shared secret for accounting.


### -field PROPERTY_RADIUSSERVER_ADDRESS

The IP address of the server, or a DNS name that corresponds to the server.


### -field PROPERTY_RADIUSSERVER_FORWARD_ACCT_ONOFF

Specifies whether to forward, that is proxy, accounting packets.


### -field PROPERTY_RADIUSSERVER_PRIORITY

Specifies the priority for server. Lower priorities have higher precedence.


### -field PROPERTY_RADIUSSERVER_WEIGHT

Specifies the weight for the server. If two servers have the same priority, then weight is used to determine which server is used.


### -field PROPERTY_RADIUSSERVER_TIMEOUT

Specifies the timeout for the server.


### -field PROPERTY_RADIUSSERVER_MAX_LOST

The number of packets that can be dropped in a row before the server is considered unavailable.


### -field PROPERTY_RADIUSSERVER_BLACKOUT

Number of seconds that are waited before checking if an unavailable server is available again.


### -field PROPERTY_RADIUSSERVER_SEND_SIGNATURE

Specifies whether the Message-Authenticator attribute of <a href="Http://go.microsoft.com/fwlink/p/?linkid=90435">RFC 3579</a>  is sent by the server or not. It is always sent for EAP authentications.


### -field PROPERTY_RADIUSSERVER_AUTH_SECRET_TEMPLATE_GUID


### -field PROPERTY_RADIUSSERVER_ACCT_SECRET_TEMPLATE_GUID




## -see-also




<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>
 

 

