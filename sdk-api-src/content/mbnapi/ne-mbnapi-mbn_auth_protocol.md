---
UID: NE:mbnapi.MBN_AUTH_PROTOCOL
title: MBN_AUTH_PROTOCOL
author: windows-sdk-content
description: The MBN_AUTH_PROTOCOL enumerated type specifies the authentication protocol used for Packet Data Protocol (PDP) activation.
old-location: mbn\mbn_auth_protocol.htm
old-project: mbn
ms.assetid: 7a1858d4-3415-490d-b264-3033cd8f5af7
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: MBN_AUTH_PROTOCOL, MBN_AUTH_PROTOCOL enumeration [Microsoft Broadband Networks], MBN_AUTH_PROTOCOL_CHAP, MBN_AUTH_PROTOCOL_MSCHAPV2, MBN_AUTH_PROTOCOL_NONE, MBN_AUTH_PROTOCOL_PAP, mbn.mbn_auth_protocol, mbnapi/MBN_AUTH_PROTOCOL, mbnapi/MBN_AUTH_PROTOCOL_CHAP, mbnapi/MBN_AUTH_PROTOCOL_MSCHAPV2, mbnapi/MBN_AUTH_PROTOCOL_NONE, mbnapi/MBN_AUTH_PROTOCOL_PAP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_AUTH_PROTOCOL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mbnapi.h
api_name:
-	MBN_AUTH_PROTOCOL
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
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

