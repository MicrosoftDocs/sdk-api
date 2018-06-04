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

# MBN_AUTH_PROTOCOL enumeration


## -description


The <b>MBN_AUTH_PROTOCOL</b> enumerated type specifies the authentication protocol used for Packet Data Protocol (PDP) activation. 

This type is applicable only for GSM devices.


## -enum-fields




### -field MBN_AUTH_PROTOCOL_NONE

No authentication protocol is used.


### -field MBN_AUTH_PROTOCOL_PAP

Password Authentication Protocol (PAP) is used for authentication. PAP authentication is unencrypted.


### -field MBN_AUTH_PROTOCOL_CHAP

Challenge Handshake Authentication Protocol (CHAP) is used for authentication.


### -field MBN_AUTH_PROTOCOL_MSCHAPV2

Microsoft Challenge-Handshake Authentication Protocol version 2.0 (MS-CHAP v2) is used for authentication.

