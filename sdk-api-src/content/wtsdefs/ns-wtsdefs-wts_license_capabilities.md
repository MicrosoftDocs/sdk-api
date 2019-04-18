---
UID: NS:wtsdefs._WTS_LICENSE_CAPABILITIES
title: WTS_LICENSE_CAPABILITIES (wtsdefs.h)
author: windows-sdk-content
description: Contains information about the licensing capabilities of the client.
old-location: termserv\wts_license_capabilities.htm
tech.root: TermServ
ms.assetid: 975a534e-03f1-4c8f-9de1-42144e31c8cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWTS_LICENSE_CAPABILITIES, PWRDS_LICENSE_CAPABILITIES, PWRDS_LICENSE_CAPABILITIES structure pointer [Remote Desktop Services], PWTS_LICENSE_CAPABILITIES, PWTS_LICENSE_CAPABILITIES structure pointer [Remote Desktop Services], WRDS_LICENSE_CAPABILITIES, WRDS_LICENSE_CAPABILITIES structure [Remote Desktop Services], WTS_KEY_EXCHANGE_ALG_DH, WTS_KEY_EXCHANGE_ALG_RSA, WTS_LICENSE_CAPABILITIES, WTS_LICENSE_CAPABILITIES structure [Remote Desktop Services], termserv.wts_license_capabilities, wtsdefs/PWRDS_LICENSE_CAPABILITIES, wtsdefs/PWTS_LICENSE_CAPABILITIES, wtsdefs/WRDS_LICENSE_CAPABILITIES, wtsdefs/WTS_LICENSE_CAPABILITIES"
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_LICENSE_CAPABILITIES
product: Windows
targetos: Windows
req.typenames: WTS_LICENSE_CAPABILITIES, *PWTS_LICENSE_CAPABILITIES
req.redist: 
ms.custom: 19H1
---

# WTS_LICENSE_CAPABILITIES structure


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



