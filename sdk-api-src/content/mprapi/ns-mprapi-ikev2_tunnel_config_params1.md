---
UID: NS:mprapi._IKEV2_TUNNEL_CONFIG_PARAMS1
title: IKEV2_TUNNEL_CONFIG_PARAMS1 (mprapi.h)
description: Used to get or set tunnel parameters for Internet Key Exchange version 2 (IKEv2) devices.
helpviewer_keywords: ["*PIKEV2_TUNNEL_CONFIG_PARAMS1","IKEV2_TUNNEL_CONFIG_PARAMS1","IKEV2_TUNNEL_CONFIG_PARAMS1 structure [RAS]","PIKEV2_TUNNEL_CONFIG_PARAMS1","PIKEV2_TUNNEL_CONFIG_PARAMS1 structure pointer [RAS]","mprapi/IKEV2_TUNNEL_CONFIG_PARAMS1","mprapi/PIKEV2_TUNNEL_CONFIG_PARAMS1","rras.ikev2_tunnel_config_params1"]
old-location: rras\ikev2_tunnel_config_params1.htm
tech.root: RRAS
ms.assetid: 0f76df0a-11f3-472a-b9ff-9a1e81c81e70
ms.date: 12/05/2018
ms.keywords: '*PIKEV2_TUNNEL_CONFIG_PARAMS1, IKEV2_TUNNEL_CONFIG_PARAMS1, IKEV2_TUNNEL_CONFIG_PARAMS1 structure [RAS], PIKEV2_TUNNEL_CONFIG_PARAMS1, PIKEV2_TUNNEL_CONFIG_PARAMS1 structure pointer [RAS], mprapi/IKEV2_TUNNEL_CONFIG_PARAMS1, mprapi/PIKEV2_TUNNEL_CONFIG_PARAMS1, rras.ikev2_tunnel_config_params1'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEV2_TUNNEL_CONFIG_PARAMS1, *PIKEV2_TUNNEL_CONFIG_PARAMS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IKEV2_TUNNEL_CONFIG_PARAMS1
 - mprapi/_IKEV2_TUNNEL_CONFIG_PARAMS1
 - PIKEV2_TUNNEL_CONFIG_PARAMS1
 - mprapi/PIKEV2_TUNNEL_CONFIG_PARAMS1
 - IKEV2_TUNNEL_CONFIG_PARAMS1
 - mprapi/IKEV2_TUNNEL_CONFIG_PARAMS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mprapi.h
api_name:
 - IKEV2_TUNNEL_CONFIG_PARAMS1
---

# IKEV2_TUNNEL_CONFIG_PARAMS1 structure


## -description

Used to get or set tunnel parameters for Internet Key Exchange version 2 (IKEv2) devices.

Do not use the <b>IKEV2_TUNNEL_CONFIG_PARAMS1</b> structure directly in your code; using <a href="/windows/desktop/RRAS/router-management-data-types">IKEV2_TUNNEL_CONFIG_PARAMS</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.

## -struct-fields

### -field dwIdleTimeout

A value that specifies the time, in seconds, after which the connection will be disconnected if there is no traffic.

### -field dwNetworkBlackoutTime

A value that specifies the retransmission timeout for IKEv2 request packets. IKEv2 expects a response for every request packet sent, this value specifies the time after which the connection is deleted in case a response is not received.

### -field dwSaLifeTime

A value that specifies the lifetime, in seconds, of a security association (SA), after which the SA is no longer valid.

### -field dwSaDataSizeForRenegotiation

A value that specifies the number of kilobytes that are allowed to be transferred using a SA before it must be renegotiated.

### -field dwConfigOptions

Not implemented. Must be set to 0.

### -field dwTotalCertificates

A value that specifies the number of certificates in the <b>certificateNames</b> member.

### -field certificateNames

An array of CERT_NAME_BLOB structures that contain X.509 public key infrastructure certificates.