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

# _WTS_LICENSE_CAPABILITIES structure


## -description


Contains information about the licensing capabilities of the client.


## -struct-fields




### -field KeyExchangeAlg

Contains an integer that specifies the encryption algorithm. This can be one of the following values.



#### WTS_KEY_EXCHANGE_ALG_RSA (1)

The RSA algorithm.



#### WTS_KEY_EXCHANGE_ALG_DH (2)

The Diffie-Hellman algorithm.


### -field ProtocolVer

An integer that specifies the supported licensing protocol. This must be <b>WTS_LICENSE_CURRENT_PROTOCOL_VERSION</b>.


### -field fAuthenticateServer

A Boolean value that specifies whether the client will authenticate the server.


### -field CertType

A <a href="https://msdn.microsoft.com/bf3dcb94-e788-4c60-ad4e-001ca040c6b0">WTS_CERT_TYPE</a> enumeration value that specifies the type of the certificate used to obtain the license.


### -field cbClientName

An integer that contains the size, in bytes, of the client name specified by the <b>rgbClientName</b> member.


### -field rgbClientName

The client name, including a terminating null character.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/ff6123f6-4d78-41d1-8093-916f01de09ef">RequestLicensingCapabilities</a> method.



