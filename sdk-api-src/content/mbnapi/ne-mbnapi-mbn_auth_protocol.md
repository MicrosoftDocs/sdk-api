---
UID: NE:mbnapi.MBN_AUTH_PROTOCOL
title: MBN_AUTH_PROTOCOL (mbnapi.h)
description: The MBN_AUTH_PROTOCOL enumerated type specifies the authentication protocol used for Packet Data Protocol (PDP) activation.
helpviewer_keywords: ["MBN_AUTH_PROTOCOL","MBN_AUTH_PROTOCOL enumeration [Microsoft Broadband Networks]","MBN_AUTH_PROTOCOL_CHAP","MBN_AUTH_PROTOCOL_MSCHAPV2","MBN_AUTH_PROTOCOL_NONE","MBN_AUTH_PROTOCOL_PAP","mbn.mbn_auth_protocol","mbnapi/MBN_AUTH_PROTOCOL","mbnapi/MBN_AUTH_PROTOCOL_CHAP","mbnapi/MBN_AUTH_PROTOCOL_MSCHAPV2","mbnapi/MBN_AUTH_PROTOCOL_NONE","mbnapi/MBN_AUTH_PROTOCOL_PAP"]
old-location: mbn\mbn_auth_protocol.htm
tech.root: mbn
ms.assetid: 7a1858d4-3415-490d-b264-3033cd8f5af7
ms.date: 12/05/2018
ms.keywords: MBN_AUTH_PROTOCOL, MBN_AUTH_PROTOCOL enumeration [Microsoft Broadband Networks], MBN_AUTH_PROTOCOL_CHAP, MBN_AUTH_PROTOCOL_MSCHAPV2, MBN_AUTH_PROTOCOL_NONE, MBN_AUTH_PROTOCOL_PAP, mbn.mbn_auth_protocol, mbnapi/MBN_AUTH_PROTOCOL, mbnapi/MBN_AUTH_PROTOCOL_CHAP, mbnapi/MBN_AUTH_PROTOCOL_MSCHAPV2, mbnapi/MBN_AUTH_PROTOCOL_NONE, mbnapi/MBN_AUTH_PROTOCOL_PAP
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_AUTH_PROTOCOL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_AUTH_PROTOCOL
 - mbnapi/MBN_AUTH_PROTOCOL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_AUTH_PROTOCOL
---

# MBN_AUTH_PROTOCOL enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_AUTH_PROTOCOL</b> enumerated type specifies the authentication protocol used for Packet Data Protocol (PDP) activation. 

This type is applicable only for GSM devices.

## -enum-fields

### -field MBN_AUTH_PROTOCOL_NONE:0

No authentication protocol is used.

### -field MBN_AUTH_PROTOCOL_PAP

Password Authentication Protocol (PAP) is used for authentication. PAP authentication is unencrypted.

### -field MBN_AUTH_PROTOCOL_CHAP

Challenge Handshake Authentication Protocol (CHAP) is used for authentication.

### -field MBN_AUTH_PROTOCOL_MSCHAPV2

Microsoft Challenge-Handshake Authentication Protocol version 2.0 (MS-CHAP v2) is used for authentication.

