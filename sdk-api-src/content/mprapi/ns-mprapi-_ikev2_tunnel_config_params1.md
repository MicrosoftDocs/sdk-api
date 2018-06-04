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

# _IKEV2_TUNNEL_CONFIG_PARAMS1 structure


## -description


Used to get or set tunnel parameters for Internet Key Exchange version 2 (IKEv2) devices.

Do not use the <b>IKEV2_TUNNEL_CONFIG_PARAMS1</b> structure directly in your code; using <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">IKEV2_TUNNEL_CONFIG_PARAMS</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


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

