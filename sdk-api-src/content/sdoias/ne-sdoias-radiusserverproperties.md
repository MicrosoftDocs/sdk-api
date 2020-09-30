---
UID: NE:sdoias._RADIUSSERVERPROPERTIES
title: RADIUSSERVERPROPERTIES (sdoias.h)
description: The values of the RADIUSSERVERPROPERTIES enumeration type enumerate the properties of the RADIUS server, that is the SDO computer.
helpviewer_keywords: ["PROPERTY_RADIUSSERVER_ACCT_PORT","PROPERTY_RADIUSSERVER_ACCT_SECRET","PROPERTY_RADIUSSERVER_ADDRESS","PROPERTY_RADIUSSERVER_AUTH_PORT","PROPERTY_RADIUSSERVER_AUTH_SECRET","PROPERTY_RADIUSSERVER_BLACKOUT","PROPERTY_RADIUSSERVER_FORWARD_ACCT_ONOFF","PROPERTY_RADIUSSERVER_MAX_LOST","PROPERTY_RADIUSSERVER_PRIORITY","PROPERTY_RADIUSSERVER_SEND_SIGNATURE","PROPERTY_RADIUSSERVER_TIMEOUT","PROPERTY_RADIUSSERVER_WEIGHT","RADIUSSERVERPROPERTIES","RADIUSSERVERPROPERTIES enumeration [Network Policy Server]","_sdo_radiusserverproperties","nps.SDO_radiusserverproperties","sdo.radiusserverproperties","sdoias/PROPERTY_RADIUSSERVER_ACCT_PORT","sdoias/PROPERTY_RADIUSSERVER_ACCT_SECRET","sdoias/PROPERTY_RADIUSSERVER_ADDRESS","sdoias/PROPERTY_RADIUSSERVER_AUTH_PORT","sdoias/PROPERTY_RADIUSSERVER_AUTH_SECRET","sdoias/PROPERTY_RADIUSSERVER_BLACKOUT","sdoias/PROPERTY_RADIUSSERVER_FORWARD_ACCT_ONOFF","sdoias/PROPERTY_RADIUSSERVER_MAX_LOST","sdoias/PROPERTY_RADIUSSERVER_PRIORITY","sdoias/PROPERTY_RADIUSSERVER_SEND_SIGNATURE","sdoias/PROPERTY_RADIUSSERVER_TIMEOUT","sdoias/PROPERTY_RADIUSSERVER_WEIGHT","sdoias/RADIUSSERVERPROPERTIES"]
old-location: nps\SDO_radiusserverproperties.htm
tech.root: Nps
ms.assetid: ff506849-0472-48a7-851f-a09f26942814
ms.date: 12/05/2018
ms.keywords: PROPERTY_RADIUSSERVER_ACCT_PORT, PROPERTY_RADIUSSERVER_ACCT_SECRET, PROPERTY_RADIUSSERVER_ADDRESS, PROPERTY_RADIUSSERVER_AUTH_PORT, PROPERTY_RADIUSSERVER_AUTH_SECRET, PROPERTY_RADIUSSERVER_BLACKOUT, PROPERTY_RADIUSSERVER_FORWARD_ACCT_ONOFF, PROPERTY_RADIUSSERVER_MAX_LOST, PROPERTY_RADIUSSERVER_PRIORITY, PROPERTY_RADIUSSERVER_SEND_SIGNATURE, PROPERTY_RADIUSSERVER_TIMEOUT, PROPERTY_RADIUSSERVER_WEIGHT, RADIUSSERVERPROPERTIES, RADIUSSERVERPROPERTIES enumeration [Network Policy Server], _sdo_radiusserverproperties, nps.SDO_radiusserverproperties, sdo.radiusserverproperties, sdoias/PROPERTY_RADIUSSERVER_ACCT_PORT, sdoias/PROPERTY_RADIUSSERVER_ACCT_SECRET, sdoias/PROPERTY_RADIUSSERVER_ADDRESS, sdoias/PROPERTY_RADIUSSERVER_AUTH_PORT, sdoias/PROPERTY_RADIUSSERVER_AUTH_SECRET, sdoias/PROPERTY_RADIUSSERVER_BLACKOUT, sdoias/PROPERTY_RADIUSSERVER_FORWARD_ACCT_ONOFF, sdoias/PROPERTY_RADIUSSERVER_MAX_LOST, sdoias/PROPERTY_RADIUSSERVER_PRIORITY, sdoias/PROPERTY_RADIUSSERVER_SEND_SIGNATURE, sdoias/PROPERTY_RADIUSSERVER_TIMEOUT, sdoias/PROPERTY_RADIUSSERVER_WEIGHT, sdoias/RADIUSSERVERPROPERTIES
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RADIUSSERVERPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUSSERVERPROPERTIES
 - sdoias/_RADIUSSERVERPROPERTIES
 - RADIUSSERVERPROPERTIES
 - sdoias/RADIUSSERVERPROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - RADIUSSERVERPROPERTIES
---

# RADIUSSERVERPROPERTIES enumeration


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

Specifies whether the Message-Authenticator attribute of <a href="https://www.ietf.org/rfc/rfc3579.txt">RFC 3579</a>  is sent by the server or not. It is always sent for EAP authentications.

### -field PROPERTY_RADIUSSERVER_AUTH_SECRET_TEMPLATE_GUID

### -field PROPERTY_RADIUSSERVER_ACCT_SECRET_TEMPLATE_GUID

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>